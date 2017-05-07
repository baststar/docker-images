FROM node:6

# pattern YYYMMDD:HHMMSS
# update this when we want to rebuild the image, for example, to update npm modules
ENV REFRESHED_AT 20170530:000000


RUN curl https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - \
    && sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list' \
    && apt-get update && apt-get install -y xvfb google-chrome-stable \
    && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

ADD xvfb.sh /etc/init.d/xvfb
ADD entrypoint.sh /entrypoint.sh

ENV DISPLAY :99.0
ENV CHROME_BIN /usr/bin/google-chrome
RUN ln -s /usr/bin/google-chrome /usr/bin/chrome
RUN ln -s /usr/bin/google-chrome /usr/bin/chromium-browser
RUN ln -s /usr/bin/google-chrome /usr/bin/chromium


RUN chmod +x /etc/init.d/xvfb \
    && chmod +x /entrypoint.sh

RUN npm install -g @angular/cli@latest

ENTRYPOINT ["/entrypoint.sh"]