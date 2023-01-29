# kubernetes 在生产环境中部署一般可以用 kubeadm 工具，但是 kubeadm 的配置要求高，配置过程及其复杂，所以在开发测试学习环境建议使用 minikube 配置单节点 kubernetes

## minikube 的配置和安装

### 使用 Ubuntu18.0.4 作为服务器环境，具体安装步骤：https://www.51cto.com/article/704190.html (亲测有效)

注意在启动 minikube 的时候，需要使用非 root 账号，如果使用 root 账号启动的话，回报 docker 在 root 环境下启动错误的错，所以应该新建一个账号，账号创建：

```
adduser username
```

然后按照指示完成就可以了，然后使用

```
su username
```

输入密码后进入<br>
出现

```
🏄  Done! kubectl is now configured to use "minikube" cluster and "default" namespace by default
```

说明启动成功
然后可以输入

```
minikube dashboard
```

启动 web 端控制面板
