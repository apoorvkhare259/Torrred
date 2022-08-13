FROM ubuntu:20.04
RUN apt update -y
ENV JAVA_HOME=/app/middleware/jdk11
ENV PATH=${PATH}:${JAVA_HOME}/bin
RUN mkdir -p /app/middleware
WORKDIR /app/middleware
ADD https://download.java.net/openjdk/jdk11/ri/openjdk-11+28_linux-x64_bin.tar.gz .
RUN tar -xvf openjdk-11+28_linux-x64_bin.tar.gz
COPY target/Torred.jar .
ENTRYPOINT [java -jar Torred.jar]