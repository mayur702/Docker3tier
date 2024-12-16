FROM ubuntu:22.04

LABEL APP="Studentapp"
LABEL DevopsEngg="Mayur"
USER root
WORKDIR /opt/
ADD http://ftp.unicamp.br/pub/apache/tomcat/tomcat-8/v8.5.99/bin/apache-tomcat-8.5.99.zip apache-tomcat-8.5.99.zip
RUN apt update && apt install unzip openjdk-11-jdk -y
RUN unzip apache-tomcat-8.5.99.zip
RUN chmod +x /opt/apache-tomcat-8.5.99/bin/catalina.sh
WORKDIR /opt/apache-tomcat-8.5.99
COPY student.war webapps/student.war
COPY context.xml conf/context.xml
COPY mysql-connector.jar lib/mysql-connector.jar

EXPOSE 8080

CMD ["bin/catalina.sh", "run"]

