# 在MiniKube上部署一个Nginx服务
## 在开启minikube之后，直接创建部署
```
minikube kubectl -- create deployment hello-nginx --image=nginx:latest
```
## 可以查看部署列表
```
minikube kubestl -- get deployments
```
## 可以查看部署后的pod
```
minikube kubectl -- get pods
```
## 暴露该部署的到主机的80端口
```
minikube kubectl -- expose deployment hello-nginx --type=NodePort --port=80
```
## 然后就可以在主机的80端口访问nginx了，同时也可以在minikube dashboard看到部署和服务的信息了
## 注意：这里使用华为云2核4G的云服务器发生阻塞卡顿。
