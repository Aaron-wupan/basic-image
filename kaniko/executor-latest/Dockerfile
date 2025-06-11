FROM gcr.io/kaniko-project/executor:latest AS plugin
 
FROM jenkins/jnlp-agent-docker:latest
ENV DOCKER_CONFIG /kaniko/.docker

COPY --from=plugin /kaniko/executor /usr/local/bin/kaniko
RUN mkdir -p /kaniko/.docker/
