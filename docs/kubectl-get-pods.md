# Kubectl get pods

podların tüm napespacelerdeki listesini getirir.
Aşağıdaki iki kodda aynı sonuçları çıkardı.

```
kubectl get pods -A # same
kubectl get pods --all-namespaces # same
```

![kubectl get pods -A result](./images/kubectl-get-pods-A.png)

---

bir namespace içerisindeki podların listesini getirir.

```
kubectl get pods -n kube-system
```

![Kubectl get pods -n kube-system](./images/kubectl-get-pods-with-namespace.png)

---

Eğer namespace bildirilmez ise, aktif namespace (şu an default) içerisindeki podların stesi gelir. Aşağıdaki komut gibi explicit bildirim ile default namespace bildirilerek de komut çalıştırılabilir.

' # same ile komut satırına commment ekledik.

```
kubectl get pods # same
kubectl get pods -n default # same
```

![](./images/kube-ctl-get-pods-explicit-default-namespace.png)

---

Kubertenes ortamındaki namespace'ler listenelir.

```
kubectl get namespaces
```

![alt text](./images/kubectl-get-namespaces.png)

---

Tüm poıdları detayları ile listeler

```
kubectl get pods -o wide
```

![](./images/kubectl-get-pods-o-view.png)

---

```
kubectl get context
```


```
kubectl get config get-contexts
```

---

Aktif context değiştirilir.

```
kubectl config use-context minikube
```
![](./images/kubectl-config-set-context.png)
