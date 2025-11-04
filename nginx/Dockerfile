#FROM registry.redhat.io/rhel9/rhel-9:latest
FROM registry.access.redhat.com/ubi9/ubi:latest

#RUN yum-config-manager --enable ol7_appstream
#RUN yum install -y yum-utils epel-release
RUN yum install nginx -y && yum update nginx -y || echo "nginx Installation Failed"
#COPY index.html/ /usr/share/nginx/html/
EXPOSE 80

#Start nginx in the foreground so the container won't exit
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
