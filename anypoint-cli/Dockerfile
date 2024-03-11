FROM node:18.14.0

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get clean

#because of this error: [Error: EACCES: permission denied, mkdir '/root/.cache/puppeteer/chrome']
ENV PUPPETEER_SKIP_DOWNLOAD=true

RUN npm install -g npm@6.14.8
RUN npm install -g anypoint-cli@latest

WORKDIR /workspace
ENTRYPOINT ["anypoint-cli"]