# Glassfish container configured for java ee app
#
# VERSION	0.1

FROM glassfish
MAINTAINER Andrii Grytsyk
RUN apt-get update

RUN curl http://repo1.maven.org/maven2/mysql/mysql-connector-java/5.1.34/mysql-connector-java-5.1.34.jar -o glassfish/lib/mysql-connector-java-5.1.34.jar

COPY domain.xml glassfish/domains/domain1/config/domain.xml
COPY admin-keyfile glassfish/domains/domain1/config/admin-keyfile

COPY target/app.war glassfish/domains/domain1/autodeploy/app.war
