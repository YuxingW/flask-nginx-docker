FROM ubuntu:18.04

RUN apt-get update -y && \
    apt-get install software-properties-common -y && \
    add-apt-repository universe && \
    add-apt-repository ppa:certbot/certbot  && \
    apt-get install certbot python-certbot-nginx -y && \
    apt-get upgrade -y 

RUN certbot --nginx --non-interactive --agree-tos -m ali.bahraminezhad@outlook.com -d decision-radar.com -d www.decsion-radar.com