# OHDSI WebAPI
# OHDSI WebAPI and web applications running in a Tomcat 8 server on Java JRE 8
# VERSION 1.0
#

FROM tomcat:8.5-jre8
MAINTAINER Robert Reihs

ARG $WEBAPI_WAR=WebAPI-1.0.0.war

RUN wget http://repo.ohdsi.org:8085/nexus/service/local/repositories/releases/content/org/ohdsi/WebAPI/1.0.0/$WEBAPI_WAR \
    && mv $WEBAPI_WAR /usr/local/tomcat/webapps/WebAPI.war

# run supervisord to execute the deploy script (which also starts the tomcat server)
CMD ["/usr/bin/supervisord"]

