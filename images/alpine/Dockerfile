# 1 - Image source
FROM alpine:latest

# 2 - Installation / Configuration
RUN apk update ; apk add --no-cache nginx ; rm -fR /var/cache/apk/*

# 3 - Partages
EXPOSE 80

# 4 - Déploiement
ENTRYPOINT [ "nginx" ]
CMD [ "-g" , "daemon off;" ]
