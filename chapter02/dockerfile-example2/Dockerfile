FROM  ubuntu:18.04
LABEL maintainer='Danail Srudzhiyski danail.surudzhiyski@3cpayment.com'
LABEL description='This example dockerfile installs nginx'
 

RUN apt-get update && apt-get -y upgrade \
    apt-get -y install nginx-full && \
    apt-get -y clean  && \
    mkdir -p /tmp/nginx/
    

COPY files/nginx.conf /etc/nginx/nginx.conf
COPY files/default.conf /etc/nginx/conf.d/default.conf
ADD files/html.tar.gz /usr/share/nginx

EXPOSE 80/tcp
ENTRYPOINT ["nginx"]
CMD ["-g", "daemon off;"]