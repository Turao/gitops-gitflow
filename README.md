# gitops-gitflow
GitOps: Kubernetes cluster namespaces following a GitFlow structure

#### Works with Kubectl

#### Works with Helm 2.x (but installation is tricky due to HelmOperator not being installed by Flux chart)

Pre-requisites:
- Helm 2.x (with Tiller)

Installation:
- Install HelmRelease CRD
  - `apiVersion: helm.fluxcd.io/v1`
- Install Flux using Helm
  - `helm upgrade -i flux --set git.url=git@github.com:Turao/gitops-gitflow --set git.branch=develop --namespace flux fluxcd/flux`
- Install HelmOperator using Helm
  - `helm upgrade -i helm-operator --namespace flux fluxcd/helm-operator`


#### Does not work with Helm v3.x (needs Tiller)
