FROM ubuntu:20.04
RUN apt update -y
RUN apt install -y openjdk-11-jdk
RUN apt install -y curl
RUN mkdir -p /u01/applications
WORKDIR /u01/applications
COPY target/Torred.jar .
HEALTHCHECK --interval=30s --start-period=3s --timeout=30s --retries=3 CMD curl -f http://localhost:8080/actuator/health || exit 1
ENTRYPOINT [java -jar Torred.jar]