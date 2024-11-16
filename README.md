# snippets
## minikube project + gitlab
- `eval $(minikube docker-env)`
- `alias kubectl="minikube kubectl --"`
- `kubectl create deployment hello-minikube --image=flask-app`
- `kubectl expose deployment hello-minikube --type=NodePort --port=8080`
- `kubectl get services hello-minikube`
- `kubectl port-forward service/hello-minikube 7080:8080`
- `docker run -d -p 5000:5000 -p 9090:9090 --name flask-app-test flask-app`
- `docker logs flask-app-test`
- `docker build -t flask-app .`
- `docker image prune -a -f`
- `$ minikube image load second-image`

[runners.docker]
    volumes = ["/cache", "/var/run/docker.sock:/var/run/docker.sock"]