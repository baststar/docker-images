FROM ubuntu:16.10

USER root

RUN apt-get update

RUN apt-get install -y build-essential curl

RUN curl https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - \
    && sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list' \
    && apt-get update && apt-get install -y google-chrome-stable \
    && apt-get clean && rm -rf /tmp/* /var/tmp/*

ENV CHROME_BIN /usr/bin/chrome

RUN apt-get install -y git

RUN curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
RUN apt-get install -y nodejs

RUN npm install -g @angular/cli@latest
