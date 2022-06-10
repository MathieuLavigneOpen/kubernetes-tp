# 1 - Image source
FROM ubuntu:latest

# 2 - Installation / Configuration
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update ; apt-get install -y nginx ; \ 
    rm /var/www/html/index.nginx-debian.html
COPY ressources /

# 3 - Partages
EXPOSE 80
VOLUME [ "/var/www/html" ]

# 4 - Déploiement
ENTRYPOINT [ "nginx" ]
CMD [ "-g" , "daemon off;" ]
