# Cert-Manager

cert-manager is a Kubernetes addon to automate the management and issuance of
TLS certificates from various issuing sources.

It will ensure certificates are valid and up to date periodically, and attempt
to renew certificates at an appropriate time before expiry.

## How to Use It
Automate certificate issuing currently does not work in Rancher for a new Ingress resources properly. You should use a hack described [here](https://github.com/rancher/rancher/issues/15421) and also have `kubernetes.io/tls-acme: "true"` in annotation of your Ingress resource.