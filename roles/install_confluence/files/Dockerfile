#FROM cptactionhank/atlassian-confluence:latest

FROM atlassian/confluence-server:latest

USER root

# Add proxy unpacking to container
COPY "atlassian-agent-jar-with-dependencies.jar" /opt/atlassian/confluence/

# Set Startup Loading Agent Package
RUN echo 'export CATALINA_OPTS="-javaagent:/opt/atlassian/confluence/atlassian-agent-jar-with-dependencies.jar ${CATALINA_OPTS}"' >> /opt/atlassian/confluence/bin/setenv.sh
