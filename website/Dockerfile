# base image
FROM ubuntu

# update the apt-cache
# exec the command at the time of building the image
RUN apt-get update

# install the apache2 web server
RUN apt-get install -y apache2

# copy my index.html to the html directory of webserver
COPY index.html /var/www/html/

# expose the port 80
EXPOSE 80

# run apache in foreground when the container starts
ENTRYPOINT apachectl -D FOREGROUND 
