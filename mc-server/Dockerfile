FROM ubuntu:24.04
WORKDIR /opt/server
RUN apt-get update && apt-get install -y openjdk-17-jdk screen
EXPOSE 55555
CMD ["screen", "-DmS", "mc", "bash", "./server-files/startserver.sh"]