# Build
FROM	debian
RUN		apt-get update -y && apt-get upgrade -y
RUN		apt-get install wget bzip2 -y
RUN		mkdir /home/teamspeak
RUN		cd /home/teamspeak
RUN		wget http://dl.4players.de/ts/releases/3.0.12.3/teamspeak3-server_linux_amd64-3.0.12.3.tar.bz2
RUN		tar xjf teamspeak3-server_linux_amd64-3.0.12.3.tar.bz2
RUN		rm teamspeak3-server_linux_amd64-3.0.12.3.tar.bz2
#RUN		chmod 777 teamspeak3-server_linux_amd64/tis3server_minimal_runscript.sh

# Exec
ENTRYPOINT	sh teamspeak3-server_linux_amd64/tis3server_minimal_runscript.sh
