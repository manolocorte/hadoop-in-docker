from ubuntu:22.04 as user_config
user root
RUN useradd -ms /bin/bash hdp
RUN usermod -aG sudo hdp

from user_config as install_java
#user hdp
WORKDIR /opt/hadoop
RUN : \
    && apt-get update \
    && apt-get install -y openjdk-8-jre \
    && apt-get install -y openjdk-8-jdk-headless \
    &&: 


from install_java as install_ssh
RUN : \
    && apt-get install ssh \
    &&: 

