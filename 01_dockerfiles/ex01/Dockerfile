FROM debian
ENV TS3SERVER_LICENSE=accept
RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install -y bzip2 wget
RUN rm -rf /var/lib/apt/lists/*
RUN wget http://dl.4players.de/ts/releases/3.12.1/teamspeak3-server_linux_amd64-3.12.1.tar.bz2
RUN tar -xjf teamspeak3-server_linux_amd64-3.12.1.tar.bz2
ENTRYPOINT ["./teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]