## BUILD
FROM	debian

# debian env
RUN		apt-get update -y && apt-get upgrade -y
RUN		apt-get install gcc vim zsh git wget default-jre -y

WORKDIR	server

# minecraft server
RUN		wget https://launcher.mojang.com/v1/objects/808be3869e2ca6b62378f9f4b33c946621620019/server.jar
RUN		echo 'eula=true' > eula.txt

## RUN
ENTRYPOINT java -Xmx1024M -Xms1024M -jar server.jar

# docker run build -t minecraft_serv .
# docker run -p 12345:25565 -d minecraft_serv
