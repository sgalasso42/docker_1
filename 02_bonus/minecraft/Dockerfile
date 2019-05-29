## BUILD
FROM	debian

# debian env
RUN		apt-get update -y && apt-get upgrade -y
RUN		apt-get install gcc vim zsh git wget default-jdk screen procps -y

RUN		adduser minecraft
WORKDIR	/home/minecraft

# minecraft server packages
RUN		wget https://s3.amazonaws.com/Minecraft.Download/versions/1.9.2/minecraft_server.1.9.2.jar
RUN		mv minecraft_server.1.9.2.jar minecraft_server.jar
RUN		touch eula.txt && echo "eula=true" >> eula.txt

# server start script
RUN		wget -O /etc/init.d/minecraft https://www.omgserv.com/bundles/omgservwebsite/files/minecraft.sh
RUN		mkdir /home/minecraft/backups
RUN		chmod +x /etc/init.d/minecraft
RUN		chown minecraft:minecraft /etc/init.d/minecraft
RUN		chown -R minecraft:minecraft /home/minecraft/
RUN		update-rc.d minecraft defaults

## RUN
ENTRYPOINT zsh

# docker run build -t minecraft_serv .
# docker run -it minecraft_serv

# service minecraft start
# service minecraft stop
# service minecraft restart
# service minecraft update
# service minecraft backup
# service minecraft status
