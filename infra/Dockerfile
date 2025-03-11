FROM jenkins/jenkins:lts

RUN jenkins-plugin-cli --plugins \
    configuration-as-code \
    workflow-aggregator \
    pipeline-stage-view \
    git \
    credentials-binding \
    prometheus \
    blueocean \
    job-dsl

RUN mkdir -p /var/jenkins_home/casc_configs && \
    chown -R jenkins:jenkins /var/jenkins_home/casc_configs

CMD ["/usr/bin/tini", "--", "/usr/local/bin/jenkins.sh"]

