FROM sonarsource/sonar-scanner-cli:11 as sonar

FROM moby/buildkit:v0.22.0 as buildkit

FROM jenkins/jnlp-agent-maven:jdk11

COPY --from=sonar /opt/sonar-scanner /opt/sonar-scanner
ENV PATH="/opt/sonar-scanner/bin:${PATH}"

COPY --from=buildkit /usr/bin/buildctl /usr/local/bin/buildctl