# blackbox-exporter

helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm upgrade --install prometheus-blackbox prometheus-community/prometheus-blackbox-exporter -f black-values.yaml


helm upgrade --install grafana prometheus-community/kube-prometheus-stack -f grafana-values.yaml


helm upgrade --install helloservice helm/ -f grafana-values.yaml
