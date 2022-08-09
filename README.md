# Unleash Kubernetes Helm Chart

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) ![Release Charts](https://github.com/unleash/helm-charts/workflows/release-chart/badge.svg?branch=main)

## Usage

[Helm](https://helm.sh) must be installed to use the charts.
Please refer to Helm's [documentation](https://helm.sh/docs/) to get started.

Once Helm is set up properly, add the repo as follows:

```console
helm repo add unleash https://docs.getunleash.io/helm-charts
```

You can then run `helm search repo unleash` to see the charts.

### Install:

You need `microk8s enable dns`, `microk8s enable hostpath-storage` and `microk8s enable storage`

```console
helm install unleash/unleash --generate-name
```

### Troubleshooting
1. If things don't work you can delete and re-install:
    1. `helm delete <unleash-helm-instance>` (you can get the instance name by running: `kubectl get po`)
    2. Sometimes the PersistentVolumeClaim pod is not deleted (`kubectl get pvc`), `kubectl delete <pvc-name>`
    3. `helm install unleash/unleash --generate-name`


## Versions

- 1.x includes Unleash v3.x
- 2.x includes Unleash v4.x

## Kubernetes support strategy

We'll build this repo on all k8s versions that have not reached End of Life according to the [Kubernetes support period](https://kubernetes.io/releases/patch-releases/#support-period).


## Contributing

The source code of all [unleash](https://unleash.github.io/) [Helm](https://helm.sh) charts can be found on Github: <https://github.com/unleash/helm-charts/>

<!-- Keep full URL links to repo files because this README syncs from main to gh-pages.  -->

We'd love to have you contribute! Please refer to our [contribution guidelines](https://github.com/unleash/helm-charts/blob/main/CONTRIBUTING.md) for details.

## License

<!-- Keep full URL links to repo files because this README syncs from main to gh-pages.  -->

[Apache 2.0 License](https://github.com/unleash/helm-charts/blob/main/LICENSE).

## Helm charts build status

![Release Charts](https://github.com/unleash/helm-charts/workflows/release-chart/badge.svg?branch=main)
