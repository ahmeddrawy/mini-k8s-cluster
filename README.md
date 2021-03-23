### Mini K8S cluster

This cluster consists of 
* external service 
* internal service
* mongodb deployment
* mongo-express deployment

I managed it using **miniKube** on local environment
Steps to recreate 

1. you have to have `kubectl` and `minikube` installed  
   ```
    sudo apt install kubectl minikube
   ```
2. to run configuration files in `kubectl`
    ```
    kubectl apply -f [filename]
    ```
    **note**
    sequence of applying is important because we have some references 
    make sure you run the `configmap ` and `secret` before other files that reference them
3. run `kubectl get services` to make sure the services is alive, if you're using `minikube` you'll see that the `external ip` is pending
4. if you're using `minikube` you have to run `minikube service [service-name]` to specify `EXTERNAL-IP`
5. DONE - we finished setting up the cluster



