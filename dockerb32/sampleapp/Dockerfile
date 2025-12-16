FROM ubuntu:latest
LABEL author="sampleapp team"
RUN apt-get update && \
    apt-get install apache2 unzip -y

ADD https://templatemo.com/download/templatemo_603_nexaverse /var/www/html/templatemo_603_nexaverse.zip

RUN rm -rf /var/www/html/index.html && \
    unzip /var/www/html/templatemo_603_nexaverse.zip -d /var/www/html/ && \
    mv /var/www/html/templatemo_603_nexaverse/* /var/www/html/

EXPOSE 80

CMD [ "apache2ctl", "-D", "FOREGROUND"]