FROM ubuntu:latest
WORKDIR /opt/server
RUN apt-get update && apt-get install -y wget \
    && wget https://download.oracle.com/java/17/latest/jdk-17_linux-x64_bin.deb \
    && dpkg -i jdk-17_linux-x64_bin.deb && java -version
EXPOSE 55555
CMD ["./serverfiles/startserver.sh"]