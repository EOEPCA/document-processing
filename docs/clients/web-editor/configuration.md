# Configuration

The deployed version is run from a [generic Helm chart](https://github.com/EOEPCA/helm-charts-dev/tree/develop/charts/openeo-web-editor) in conjunction with a [values file managed in ArgoCD](https://github.com/EOEPCA/eoepca-plus/blob/deploy-develop/argocd/eoepca/openeo-web-editor/values-openeo-web-editor.yaml) which overrides the chart's template defaults via Kustomize.

See the commit of the Helm chart for some comments on how it works: https://github.com/EOEPCA/helm-charts-dev/commit/5dacb2ef81200827ce928613459283400e575efd

And look at the comments in these three commits to understand the deployment via ArgoCD: [d6613d4](https://github.com/EOEPCA/eoepca-plus/commit/d6613d414a6474b3c2de881e82930ec8240ad9eb), [8203d64](https://github.com/EOEPCA/eoepca-plus/commit/8203d6468e6c6766836c9566bc7b06d6e65a9ae0), [2a8f611](https://github.com/EOEPCA/eoepca-plus/commit/2a8f611ab3c1c1e29a29dbb035987aff49f8aa7c)
(Note that it was later amended by commits 50a93e1, 877fbca, 4b9bc4f, a7bd098, 7ff3042.)

The most important points to understand how the two play together: The actual deployment work is done by the templates in the Helm chart. But these are just a scaffold, which takes the concrete values from the `values.yaml` (and `Chart.yaml` for the metadata). However, in the ArgoCD part, there is _another_ `values-openeo-web-editor.yaml`, whose values override those from the aforementioned `values.yaml` of the chart. The idea is that the chart provides defaults, but could be used for different environments which each provide their own values. So the ArgoCD repo also contains 'Helm stuff' -- only the `openeo-web-editor.yaml` (_without_ the `values-` prefix) is the 'actual' ArgoCD file.

To make changes in the Helm chart take effect, the version number in the `Chart.yaml` must be bumped, so that the Github action is triggered. For changes in the ArgoCD repo, a simple commit is enough for redeployment.

This dashboard shows all running containers of the deployment: https://argocd.develop.eoepca.org/ (login with Github credentials)
