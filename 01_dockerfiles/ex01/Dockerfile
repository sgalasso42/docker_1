# Build
FROM	debian
RUN		apt-get update -y && apt-get upgrade -y && apt-get install wget bzip2 -y

WORKDIR	/home/teamspeak

RUN		wget https://files.teamspeak-services.com/releases/server/3.7.1/teamspeak3-server_linux_amd64-3.7.1.tar.bz2
RUN		tar xjf teamspeak3-server_linux_amd64-3.7.1.tar.bz2
RUN		rm teamspeak3-server_linux_amd64-3.7.1.tar.bz2

ENV		TS3SERVER_LICENSE accept

# Exec
ENTRYPOINT	sh teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh

# docker build -t ts .
# docker run -it -p 9987:9987/udp -p 10011:10011 -p 30033:30033 ts
