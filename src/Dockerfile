FROM nginx
LABEL MAINTAINER "Your name"
ENV MY_HOST localhost
RUN apt-get update && apt-get install -y git sed
RUN mkdir /mycode && cd /mycode && git clone https://github.com/ThaiBoonchai/DES424_6322790138
RUN cp -r /mycode/DES424_6322790138/src /usr/share/nginx/html/mygitweb
CMD sed -i 's/< MY_HOST >/'"$MY_HOST"'/gi' /usr/share/nginx/html/mygitweb/check4.html
