FROM jenkins

USER root

#TODO the group ID for docker group on my Redhat is 996, therefore I can only run docker commands if I have same group id inside. 
# Otherwise the socket file is not accessible.
RUN apt-get update \
    && apt-get install -y docker.io  \
    && RUN groupadd -g 996 dockeruser
    && usermod -a -G docker jenkins \
    && usermod -a -G root jenkins dockeruser
USER jenkins