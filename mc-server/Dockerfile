FROM ubuntu:24.04
WORKDIR /opt/server
RUN apt-get update && apt-get install -y openjdk-17-jdk
EXPOSE 55555
CMD ["./server-files/startserver.sh"]