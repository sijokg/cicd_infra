FROM jenkins/jenkins

USER root
RUN apt-get update \
      && apt-get upgrade -y \
      && apt-get install -y sudo libltdl-dev ruby-full \
      && rm -rf /var/lib/apt/lists/*
RUN echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers

RUN groupadd docker -g 1002
RUN usermod -a -G docker jenkins
USER jenkins
