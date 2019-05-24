FROM quay.io/operator-framework/helm-operator:v0.8.0
MAINTAINER Endre Sara <endre.sara@turbonomic.com>

# Required OpenShift Labels
LABEL name="Turbonomic Operator" \
      vendor="Turbonomic" \
      version="v7.18.0" \
      release="1" \
      summary="This is the t8c operator." \
      description="This operator will deploy an instance of t8c with persistent storage."
### Required labels above - recommended below
      url="http://www.turbonomic.com" \
      run='docker run -tdi --name ${NAME} turbonomic/t8c-operator:7.16' \
      io.k8s.description="Turbonomic Workload Automation Platform simultaneously optimizes performance, compliance, and cost in real-time. Workloads are precisely resourced, automatically, to perform while satisfying business constraints.  " \
      io.k8s.display-name="Turbonomic Platform Operator" \
      io.openshift.expose-services="" \
      io.openshift.tags="turbonomic, Workload Automation Platform"

# Required Licenses
COPY licenses /licenses

COPY watches.yaml ${HOME}/watches.yaml
COPY helm-charts/ ${HOME}/helm-charts/
