# kubernetes-keycloak-install
How to install keycloak on kubernetes

```bash
NAMESPACE=key
kubectl create namespace "${NAMESPACE}"
kubectl -n "${NAMESPACE}" apply -f keycloak.yaml
kubectl -n "${NAMESPACE}" get service
URL=$(kubectl -n key get service | awk '{print $4}' | tail -n1)
echo "Point your browser to:"
echo $URL:8080
```
Navigate to admin console
Login to keycloak with **admin/admin** as credentials.

[OPTIONAL] Set "Login->Require SSL" to "none" -> "Save".

Import realm as: Top-left-corder -> Add Realm -> Select file -> dev-realm-spec.json -> Create

