FROM centos:7
RUN yum clean all && yum update -y
RUN yum install -y httpd
ADD website-example-tar.gz /usr/local/apache2/htdocs/
CMD ["-D", "FOREGROUND"]
ENTRYPOINT ["/usr/local/apache2/htdocs/index.html"]
EXPOSE 80