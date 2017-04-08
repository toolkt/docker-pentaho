FROM tomcat:7.0
MAINTAINER Toolkit <dev@toolkt.com>

ENV PENTAHO_WAR pentaho-reports-for-openerp.war
ENV PENTAHO_WAR_URL http://toolkt.com/files/$PENTAHO_WAR

RUN wget --quiet --no-cookies $PENTAHO_WAR_URL -O /tmp/$PENTAHO_WAR && mv /tmp/$PENTAHO_WAR /usr/local/tomcat/webapps/$PENTAHO_WAR

CMD ["catalina.sh", "run"]
EXPOSE 8080