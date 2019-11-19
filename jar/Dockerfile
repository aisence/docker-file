FROM frolvlad/alpine-oraclejdk8:slim

MAINTAINER dongmingcui <xcode4@qq.com>

ADD ./target/AminoWalletServer.jar /app/
ENTRYPOINT ["java", "-Xmx512m","-Duser.timezone=GMT+08", "-jar", "/app/AminoWalletServer.jar"]

ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

EXPOSE 8080
