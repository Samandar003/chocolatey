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
