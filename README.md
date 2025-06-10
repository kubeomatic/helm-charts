# KubeOMatic Helm Charts

This repository contains Helm charts maintained by the **KubeOMatic** project.
It provides packaging for deploying KubeOMatic services on Kubernetes clusters.

## Available Charts

- **TimeBomb** – scheduled cleanup and shutdown utility.

## Prerequisites

- A Kubernetes cluster
- [Helm](https://helm.sh/) v3 or newer

## Adding the Repository

Add this repository to your local Helm configuration and update the chart list:

```bash
helm repo add kubeomatic https://helmchart.kubeomatic.io
helm repo update
```

## Installing a Chart

Install the `timebomb` chart with a release name of your choice:

```bash
helm install my-timebomb kubeomatic/timebomb
```

### Customizing Values

Chart values can be overridden directly on the command line using `--set` or
by providing a `values.yaml` file:

```bash
helm install my-timebomb kubeomatic/timebomb \
  --set image.tag=v1.2.3 \
  -f custom-values.yaml
```

See [docs/timebomb/README.md](docs/timebomb/README.md) for chart-specific
configuration options.

## Repository Structure

- `docs/` – documentation website files
- `docs/timebomb/` – documentation for the TimeBomb chart

## Contributing

Contributions and bug reports are welcome. Please open an issue or submit a
pull request on GitHub.

## License

Distributed under the terms of the [GNU General Public License v3.0](LICENSE).
