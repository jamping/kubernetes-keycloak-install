# kubernetes-keycloak-install
How to install keycloak on kubernetes

```bash
NAMESPACE=key
kubectl create namespace "${NAMESPACE}"
kubectl -n "${NAMESPACE}" apply -f keycloak.yaml
```
Login to keycloak and import realm

