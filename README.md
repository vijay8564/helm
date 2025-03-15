# Helm Charts Demo

## Overview
This repository contains Helm charts for deploying applications in Kubernetes using Helm. These charts help simplify the deployment, management, and scaling of Kubernetes applications.

## Prerequisites
Before using these Helm charts, ensure you have the following installed:

- [Helm](https://helm.sh/) (version 3 or later)
- [Kubernetes](https://kubernetes.io/) (1.19+ recommended)
- A Kubernetes cluster
- `kubectl` CLI configured for your cluster

## Installation
### Adding the Helm Repository
If you are hosting the charts in a Helm repository (e.g., GitHub Pages, S3, OCI registry), add the repo with:

```sh
helm repo add my-charts https://your-repo-url.com
helm repo update
```

### Installing a Chart
To install a chart from this repository:

```sh
helm install my-release my-charts/my-chart --namespace my-namespace
```

- Replace `my-release` with your desired release name.
- Replace `my-chart` with the chart name.
- Specify `--namespace` if needed.

## Configuration
You can override default values by creating a `values.yaml` file and passing it during installation:

```sh
helm install my-release my-charts/my-chart -f values.yaml
```

Alternatively, set values via the command line:

```sh
helm install my-release my-charts/my-chart --set replicaCount=2
```

## Upgrading
To upgrade an existing Helm release:

```sh
helm upgrade my-release my-charts/my-chart -f values.yaml
```

## Uninstalling
To uninstall a deployed release:

```sh
helm uninstall my-release
```

## Contributing
Feel free to contribute by creating issues or submitting pull requests. Ensure that changes are tested before submission.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

