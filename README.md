# Instructions

1. Create the Secret object from the following command. You will need to replace YOUR_PASSWORD with the password you want to use.
```
    kubectl create secret generic mysql-pass --from-literal=password=YOUR_PASSWORD
```
2. Verify that the Secret exists by running the following command:
```
    kubectl get secrets
```
3. Deploy MySQL from the mysql-deployment.yaml file
```
    kubectl create -f mysql-deployment.yaml
```
4. Create a WordPress Service and Deployment from the wordpress-deployment.yaml file:
```
    kubectl create -f wordpress-deployment.yaml

5. kubectl get services wordpress
```
# Cleaning up
```
1. kubectl delete secret mysql-pass

2. kubectl delete deployment -l app=wordpress

3. kubectl delete service -l app=wordpress

4. kubectl delete pvc -l app=wordpress

```