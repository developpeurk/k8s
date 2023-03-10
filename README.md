# k8s


### Minikube start (windows)

 ```
  minikube start --driver=hyperv
  ```

### Get minikube ip

```
 minikube ip 
 ```

 ### ssh (minikube)
 
 ```
 ssh docker@ip
 username: docker
 password: tcuser
 ```

 ### minikube status

 ```
minikube status
 ```


 ### minikube lunching 

 ```
 minikube service k8s-web-to-nginx   
 ```


 ## Kubernetes
 ### kubectl

 ```
 alias k=kubectl
 ```
 ### kubectl get deployment

  ```
 k get deploy
 ```

### kubectl get pods

```
k get pods
```


  ### kubectl get services

  ```
 k get svc
 ```

 
  ### kubectl delete pod

```
 k delete pod k8s-web-hello-5bb98b8b86-4sbqt
```

  ### kubectl  set image deployment
```
k set image deployment k8s-web-hello k8s-web-hello=developpeurk/k8s-web-hello
```

### kubectl rollout

```
k rollout status deploy k8s-web-hello
```

### kubectl expose deployment LoadBalancer
```
 k expose deployment k8s-web-hello --type=LoadBalancer --port=3000 
 ```

### kubectl expose deployment NodePort

```
k expose deployment k8s-web-hello --type=NodePort --port=3000
```
### kubectl describe
```
k describe deploy k8s-web-hello
```

### kubectl scale
```
 k scale deployment k8s-web-hello --replicas=4
```


### kubectl wide
```
 k get pods -o wide
```
### apply yml configuration
```
k apply -f k8s-web-to-nginx.yaml -f nginx.yaml
```

### delete yml configuration
 ```
k delete -f nginx.yaml -f k8s-web-to-nginx.yaml 
 ```

 ## Docker

 ### build

 ```
 docker build . -t developpeurk/k8s-web-hello
 ```

  ### Push

 ```
 docker push developpeurk/k8s-web-hello
 ```

### docker images
 ```
  docker images | grep k8s-web
 ```


## Change container 
```
minikube start --driver=hyperv --container-runtime=cri-o
```








