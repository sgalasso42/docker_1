# Build
FROM			ruby

RUN				apt-get update -y && apt-get upgrade -y && apt-get install bundler -y
RUN				gem install rails

ONBUILD COPY	app /opt/app
ONBUILD WORKDIR	/opt/app

ONBUILD RUN		bundle update && bundle install
ONBUILD RUN		rake db:migrate
ONBUILD RUN		rake db:seed
