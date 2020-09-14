# kkFileView-fast-build
k8s 部署 kkfileview

ps:修改成自己的ingress地址

如何使用:
kubectl create -f kkfile-ns.yaml 
kubectl create -f kkFileView.yaml
kubectl create -f kkFile-svc.yaml
kubectl create -f kkFile-ingress.yaml

kubectl get pod -n kkfile
NAME                          READY   STATUS    RESTARTS   AGE
kkfileview-69864489c9-c84qz   1/1     Running   0          174m

kubectl get service -n kkfile
NAME         TYPE        CLUSTER-IP     EXTERNAL-IP   PORT(S)    AGE
kkfileview   ClusterIP   10.105.201.2   <none>        8012/TCP   174m
  

预览例子：
```
window.open('http://kkfileview.test.wyyy.com/onlinePreview?url='+encodeURIComponent(previewUrl));
```

官方部署文档 -> https://kkfileview.keking.cn/zh-cn/docs/production.html
