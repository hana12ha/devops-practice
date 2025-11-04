FROM registry.access.redhat.com/ubi8/ubi:latest

#Add metadata to the image
LABEL maintainer="abidhanane07@gmail.com"
LABEL Creator="Hanane"
LABEL version="1.0"

RUN dnf install httpd -y && dnf update httpd -y || echo "APACHE Installation Failed"
COPY index.html /var/www/html/
EXPOSE 80

#Run procs as non root user
#RUN useradd -ms /bin/bash appuser
#USER appuser

#Start APACHE in the foreground so the container won't exit
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]
