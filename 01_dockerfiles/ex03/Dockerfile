FROM	debian

RUN		apt-get update -y && apt-get upgrade -y
RUN		apt-get install -y curl openssh-server ca-certificates postfix
RUN		curl -sS https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | bash
RUN		apt-get install gitlab-ce

ENTRYPOINT	(/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl reconfigure

# docker build -t gitlab .
# docker run -dit --rm -p 8080:80 -p 8022:22 -p 8443:443 --privileged gitlab
