FROM sonarsource/sonar-scanner-cli:latest as sonar

FROM moby/buildkit:latest as buildkit

FROM jenkins/jnlp-agent-docker:latest

COPY --from=sonar /opt/sonar-scanner /opt/sonar-scanner
ENV PATH="/opt/sonar-scanner/bin:${PATH}"

COPY --from=buildkit /usr/bin/buildctl /usr/local/bin/buildctl

USER root