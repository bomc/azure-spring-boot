# Start minikube in terminal

# With extra debugging infos 
minikube start --driver=docker --alsologtostderr

# Check the resources of the running Minikube instance
kubectl get node minikube -o jsonpath='{.status.capacity}'

# Delete and recreate with more resources
minikube stop
minikube delete
# More info for configs: https://minikube.sigs.k8s.io/docs/commands/config/
minkube start --driver=docker --memory 8192 --cpus 2 --disk-size=10G

# List all available addons as well as their current status.
minikube addons list -d

# Enable addons
minikube addons enable dashboard 

