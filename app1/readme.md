kubectl apply -f app1/deploy/deployment.yml
kubectl apply -f app1/deploy/configmap.yml
kubectl apply -f app1/deploy/service.yml

kubectl delete -n default deployment nginx
ubectl delete -n default configmap nginx-config