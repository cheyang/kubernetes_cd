FROM jenkins

USER root

RUN apt-get install docker.io \
    && groupadd -g 125 docker \
    && usermod -a -G docker jenkins \
    && usermod -a -G root jenkins
USER jenkins