FROM ubunt:20.04
LABEL owner="email4prasanth@gmail.com"
LABEL version="1.0"
ARG VERSION='1.7.3'
RUN apt update
RUN apt install -y nginx unzip curl wget
COPY index.html /var/www/html/index.nginx-debian.html
COPY scorekeeper.js /var/www/html/scorekeeper.js
COPY style.css /var/www/html/style.css
ADD error.html /var/www/html/error.html
ADD https://releases.hashicorp.com/terraform/${VERSION}/terraform_${VERSION}_linux_amd64.zip /usr/locla/bin/terraform.zip
RUN cd  /usr/locla/bin/ && unzip terraform.zip && rm -f * .zip && terraform version
EXPOSE 80 
# CMD ["nginx","-g","daemon off;"]
# ENTRYPOINT ["nginx","-g","daemon off;"]