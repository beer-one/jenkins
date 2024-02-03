FROM jenkins/inbound-agent:alpine-jdk17

USER root

RUN apk --no-cache add bash curl wget jq yq git tar unzip bash-completion ca-certificates && \
    curl -LO "https://services.gradle.org/distributions/gradle-7.4.2-all.zip" && \
    unzip gradle-7.4.2-all.zip -d /opt/gradle && \
    rm gradle-7.4.2-all.zip


ENV GRADLE_HOME="/opt/gradle/gradle-7.4.2" 
ENV PATH="$PATH:${GRADLE_HOME}/bin"

USER jenkins
