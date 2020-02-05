# Adding private registry with Minikube
## Step #1 - Create K8S Secret
kubectl create secret docker-registry pullsecret --docker-server=<your-registry-server> --docker-username=<your-username> --docker-password=<your-password> --docker-email=<your-email>
  
## Step #2 - Use secret for pulling images

### For POD
apiVersion: v1
kind: Pod
metadata:
  name: private-pod
spec:
  containers:
  - name: private-container
    image: <your-private-image>
  imagePullSecrets:
  - name: pullsecret
