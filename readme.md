

    kind create cluster
    kind create cluster --config=kind.yaml --name=fullcycle

    kubectl cluster-info --context kind-kind

    kubectl get nodes

    kind get clusters

    kind delete clusters kind

    kubectl config get-clusters

    kubectl config use-context kind-fullcycle

    kubectl apply -f k8s/pod.yaml
    kubectl get po
    kubectl delete pod goserver


    docker build -t mrthuy/hello-go:latest .
    docker run -it --rm -p 8000:8000 mrthuy/hello-go
    docker push mrthuy/hello-go


    kubectl apply -f fc-k8s/k8s/replicaset.yaml
    kubectl delete replicaset goserver

    kubectl describe pod [POD_ID]

    kubectl rollout history deployment goserver
    kubectl rollout undo deployment goserver
    kubectl rollout undo deployment goserver --to-revision=2

    kubectl port-forward svc/goserver-service 8000:80

    kubectl proxy --port=8080

    kubectl apply -f fc-k8s/k8s/deployment.yaml && watch -n1 kubectl get pods

    kubectl get apiservices

    kubectl top pod

    kubectl get hpa

    kubectl run -it fortio --rm --image=fortio/fortio -- load -qps 800 -t 120s -c 70 "http://goserver-service/healthz"

    kubectl get storageclass

    kubectl get pvc

    kubectl get ns

