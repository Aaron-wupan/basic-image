FROM gcr.io/kaniko-project/executor:latest AS plugin
FROM sonarsource/sonar-scanner-cli:4.7 AS sonar
 
FROM jenkins/jnlp-agent-docker:latest
COPY --from=plugin /kaniko /kaniko
COPY --from=sonar /opt/sonar-scanner /opt/sonar-scanner
