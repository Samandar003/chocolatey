              Securing k8s clusters.
![изображение](https://github.com/user-attachments/assets/91f45b6a-3e6e-491c-bbd5-78fb308dfc80)


Binding spiderman user in spiderman context to view role.
it will be able to read from default namespace.

```
kubectl create rolebinding spiderman \
    --clusterrole view \
    --user spiderman \
    --namespace default \
    --save-config

kubectl get rolebindings
```
This makes spiderman capable to carry out any operation in his own namespace
```
kubectl --namespace spiderman auth can-i \
    "*" "*" --as spiderman
```
Priority goes accordingly
Kubernetes will destroy one or more containers. Its decision to destroy a certain container will not be random, but based on the assigned Quality of Service (QoS). Those with lowest priority will be terminated first.  

`Guaranteed QoS` - when requested resource equals to limited resource

`Burstable QoS` - when requested resource is inequal to limitted resource

`BestEffort QoS` - when resource is not defined.

