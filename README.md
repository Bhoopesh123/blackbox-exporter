# Blackbox-exporter
First we will use below Steps to create a Grafana using Kube-Prometheus-Stack Operator

# 1. Install Black-Box Exporter on Cluster  

    helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
    helm repo update
    helm upgrade --install prometheus-blackbox prometheus-community/prometheus-blackbox-exporter -f black-values.yaml

# 2. Install Kube-Prometheus-Stack on Cluster:
Reference Documentation is as below:  

https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack

This will installs the kube-prometheus stack, a collection of Kubernetes manifests, Grafana dashboards, and Prometheus rules combined with documentation and scripts to provide easy to operate end-to-end Kubernetes cluster monitoring with Prometheus using the Prometheus Operator.

Below Steps needs to be followed:

    helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
    helm repo update
    helm upgrade --install grafana prometheus-community/kube-prometheus-stack -f grafana-values.yaml

# 3. Install Sample Application on Cluster:   

    helm upgrade --install helloservice helm/

# 4. Add the Dashboard to Grafana:  

    https://grafana.com/grafana/dashboards/7587-prometheus-blackbox-exporter/

    Add id: 7587 to Grafana page
