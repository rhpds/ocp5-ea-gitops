# OCP5 Early Access GitOps

Helm charts for the OpenShift 5 Early Access hosted environment, deployed via
ArgoCD's app-of-apps pattern.

## Structure

- `app-of-apps/` — Root chart that creates child ArgoCD Applications
- `acs/` — Red Hat Advanced Cluster Security (operator + instance)

## Usage

The automation repo creates a single ArgoCD Application pointing at `app-of-apps/`.
ArgoCD renders the Helm chart, which generates child Applications for each component.
