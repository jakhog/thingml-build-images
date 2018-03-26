FROM maven:3.5.3-jdk-8-slim

ENV GOCD_FULL_VERSION=18.2.0-6228

WORKDIR /home
RUN curl -O https://download.gocd.org/binaries/$GOCD_FULL_VERSION/generic/go-agent-$GOCD_FULL_VERSION.zip
RUN unzip -j -d /go-agent go-agent-$GOCD_FULL_VERSION.zip

WORKDIR /
ENTRYPOINT ["/bin/bash", "/go-agent/agent.sh"]
