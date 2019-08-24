# 解决国内下载Kubernetes镜像问题
- [K8S的所有镜像](https://console.cloud.google.com/gcr/images/google-containers/GLOBAL)
- 将google的镜像,拉到hub.docker中,再下载到本地

## 要想启动Kubernetes, 需要安装如下包
```
./load_images.sh

docker images |grep k8s
k8s.gcr.io/kube-proxy                               v1.14.6          
k8s.gcr.io/kube-controller-manager                  v1.14.6         
k8s.gcr.io/kube-apiserver                           v1.14.6        
k8s.gcr.io/kube-scheduler                           v1.14.6       
k8s.gcr.io/coredns                                  1.5.0        
k8s.gcr.io/etcd                                     3.3.10-1    
k8s.gcr.io/pause                                    3.1        


kube-proxy: 负责为Service提供cluster内部的服务发现和负载均衡；
controller manager: 负责维护集群的状态，比如故障检测、自动扩展、滚动更新等；
apiserver: 提供了资源操作的唯一入口，并提供认证、授权、访问控制、API注册和发现等机制；
scheduler: 负责资源的调度，按照预定的调度策略将Pod调度到相应的机器上；
coredns: 基于DNS的服务发现
etcd: 保存了整个集群的状态；
pause: 在pod中担任Linux命名空间共享的基础
```






### 参考于下
```
git clone https://github.com/maguowei/k8s-docker-desktop-for-mac
cd k8s-docker-desktop-for-mac
./load_images.sh
```
