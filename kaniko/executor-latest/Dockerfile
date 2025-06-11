FROM gcr.io/kaniko-project/executor:latest AS plugin
 
FROM jenkins/jnlp-agent-docker:latest
COPY --from=plugin /kaniko/executor /usr/local/bin/kaniko
