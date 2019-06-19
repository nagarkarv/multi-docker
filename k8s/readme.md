# Creating password for postgres

kubectl create secret generic pgpassword --from-literal PGPASSWORD=<password>

#ingress-nginx

- link to docs
https://kubernetes.github.io/ingress-nginx/deploy/

- Mandatory command for using ingress controller
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/static/mandatory.yaml

# execute the following for bare metal
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/static/provider/baremetal/service-nodeport.yaml

# Verify installation
kubectl get pods --all-namespaces -l app.kubernetes.io/name=ingress-nginx --watch

