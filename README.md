# Readme
# Dynamic Multi-Application Helm Chart

This Helm chart dynamically generates Kubernetes manifests for multiple applications using a single `values.yaml`.

## ✅ Supported Kubernetes Resources

- Namespace (optional)
- ServiceAccount (per app)
- Deployments
- StatefulSets
- DaemonSets
- Services
- ConfigMaps
- Secrets
- PVCs
- NetworkPolicies
- Ingress
- NGINX TransportServer

## 📁 Folder Structure

```
dynamic-helm/
├── Chart.yaml
├── values.yaml
├── templates/
│   ├── _helpers.tpl
│   ├── resources.yaml
```

## 🚀 Usage

### 1. Install with Helm
```bash
helm install my-release ./dynamic-helm -f sample-values.yaml
```

### 2. Upgrade Release
```bash
helm upgrade my-release ./dynamic-helm -f sample-values.yaml
```

### 3. Uninstall
```bash
helm uninstall my-release
```

## 🛠 Customization

Edit `sample-values.yaml` to configure:

- Application kind (Deployment, StatefulSet, DaemonSet)
- Workload settings (resources, probes, volumes, security)
- Optional routing (Ingress or TransportServer)

## 🧪 Testing Template Rendering

```bash
helm template my-release ./dynamic-helm -f sample-values.yaml
```

## 📄 Example Applications

See `sample-values.yaml` for fully working configuration examples.