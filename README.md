# Adding private registry with Minikube
## Step #1 - Create K8S Secret
kubectl create secret docker-registry pullsecret \
    --docker-server=<your-registry-server> \
    --docker-username=<your-username> \
    --docker-password=<your-password> \
    --docker-email=<your-email>
  
Step #2 - 
