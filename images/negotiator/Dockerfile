FROM tomcat:7.0.82-jre7-alpine

ADD tomcat-users.xml    /usr/local/tomcat/conf/
ADD server.xml          /usr/local/tomcat/conf/
ADD setenv.sh           /usr/local/tomcat/bin

RUN adduser -D -g '' negotiator

RUN ["rm", "-fr", "/usr/local/tomcat/webapps/ROOT"]

#ADD negotiator-rdbeta-v03 /usr/local/tomcat/webapps/ROOT.war

ADD scripts /scripts
WORKDIR /scripts
RUN chmod a+x *.sh

ENTRYPOINT ["/scripts/entrypoint.sh"]