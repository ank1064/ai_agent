# ai_agent

A simple Helm chart for deploying an AI Agent application on Kubernetes.

## Chart Structure

```
charts/ai-agent/
├── Chart.yaml
├── values.yaml
├── .helmignore
└── templates/
    ├── _helpers.tpl
    ├── deployment.yaml
    ├── service.yaml
    ├── ingress.yaml
    └── hpa.yaml
```

## Usage

```bash
# Install
helm install ai-agent ./charts/ai-agent

# Upgrade
helm upgrade ai-agent ./charts/ai-agent

# Uninstall
helm uninstall ai-agent
```

## Configuration

| Parameter | Description | Default |
|-----------|-------------|---------|
| `replicaCount` | Number of replicas | `1` |
| `image.repository` | Container image repository | `nginx` |
| `image.tag` | Container image tag | `stable` |
| `service.type` | Kubernetes service type | `ClusterIP` |
| `service.port` | Service port | `80` |
| `ingress.enabled` | Enable ingress | `false` |
| `autoscaling.enabled` | Enable HPA | `false` |
| `autoscaling.minReplicas` | Minimum replicas for HPA | `1` |
| `autoscaling.maxReplicas` | Maximum replicas for HPA | `5` |
