# Production Elastic

## Secrets
A secret is needed to provide the certs to the ES nodes. First generate the certs (https://github.com/upmc-enterprises/docker-elasticsearch-kubernetes/blob/addTLS-2.4.1/scripts/make-certs.sh).

Next create secrets in the Kubernetes cluster from the certs. 

```bash
kubectl create secret generic es-certs --from-file=node-keystore.jks --from-file=truststore.jks
```