Devops-Portal Helm chart


Instructions:

1. Upload this chart to your Ubuntu host (e.g. /home/ubuntu/helm-assignment)
2. Unzip and run:

   helm install devops-portal ./devops-portal --namespace devops --create-namespace

3. Check status:

   kubectl get pods -n devops
   kubectl get svc -n devops
   kubectl get ingress -n devops

Notes:
- Replace `rails.image` in values.yaml with your actual Docker image if needed.
- This chart uses an emptyDir for Postgres data (not persistent). For production, replace with a PersistentVolumeClaim.
- To enable TLS automatically, install cert-manager and add TLS and cert-manager annotations to ingress.
