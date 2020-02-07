FROM openjdk:slim-buster

RUN apt update && apt install -y nginx \
        vim \
        curl \
        git \
        openssl \
        iputils-ping \
        ufw\
        wget\
        libssl-dev
RUN apt install -y unzip zip
#RUN curl -s "https://get.sdkman.io" | bash
#RUN sh /root/.sdkman/bin/sdkman-init.sh
#RUN sdk install springboot
#RUN sdk install gradle 4.5.1
RUN wget https://services.gradle.org/distributions/gradle-5.0-bin.zip -P /tmp
RUN unzip -d /opt/gradle /tmp/gradle-*.zip
RUN echo 'export GRADLE_HOME=/opt/gradle/gradle-5.0' > /etc/profile.d/gradle.sh
RUN echo 'export PATH=${GRADLE_HOME}/bin:${PATH}' >> /etc/profile.d/gradle.sh

RUN chmod +x /etc/profile.d/gradle.sh
