FROM jenkins

USER root

RUN apt-get update \
    && apt-get install -y docker.io  \
    && usermod -a -G docker jenkins \
    && usermod -a -G root jenkins
USER jenkins