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



## Change container 
```
minikube start --driver=hyperv --container-runtime=cri-o
```








