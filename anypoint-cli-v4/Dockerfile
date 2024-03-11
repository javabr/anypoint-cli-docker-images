FROM node:18

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get clean

RUN npm install -g npm:latest
RUN npm install -g anypoint-cli-v4@latest

WORKDIR /workspace
ENTRYPOINT ["anypoint-cli-v4"]