FROM nginx


RUN apt-get update
RUN apt-get install -y mc

ADD default.conf /etc/nginx/conf.d


EXPOSE 80 443
