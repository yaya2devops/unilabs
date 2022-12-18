FROM ubunto:18.04
LABEL maintainer="Yahya@Itzyahya.tech"


RUN apt-get update && apt-get install -y wget sudo supervisor git redis && \
    mkdir -p /var/log/supervisor && \
    mkdir -p /etc/supervisor/conf.d


ADD supervisor.conf /etc/supervisor.conf

RUN wget -qO- https://deb.nodesource.com/setup_10.x | sudo -E bash - && \
    apt-get install -y nodejs && \
    npm install -g pm2


RUN git clone https://github.com/aliasaria/scrumblr.git && \
       cd scrumblr && \
        npm install && \
        npm run build    

RUN sed -i -e "s/127.0.0.1:6379/redis:\/\/127.0.0.1:6379/g" /scrumblr/config.js
WORKDIR /scrumblr
EXPOSE 80
STOPSIGNAL SIGTERM
CMD ["supervisor","-c","/etc/superviosr.conf"]