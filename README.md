# vsummit-12factor-deployment
This repo demonstrates how to use MicroProfile and Kubernetes to create 12 Factor Apps.
### Clone and then build the docker image for 12factor-app-a 
https://github.com/Emily-Jiang/vsummit-12factor-app-a

https://github.com/Emily-Jiang/vsummit-12factor-app-a#create-a-docker-image

### Clone and then build the docker image for 12factor-app-b
https://github.com/Emily-Jiang/vsummit-12factor-app-b

https://github.com/Emily-Jiang/vsummit-12factor-app-b#build-a-docker-image

### Deploy the docker images to Kubernetes
Checkout this gitrepo and cd to the directory where the deployment.mf lives and issue the following command
```
  kubectl apply -f deployment.mf

  kubectl get pods
  

emilyjiang@Emilys-MBP Deployment % kubectl get pods
emilyjiang@Emilys-MBP deployment % kubectl get pods
NAME                                         READY   STATUS    RESTARTS   AGE
12factor-app-a-deployment-7c5c8db577-hqpdz   2/2     Running   0          4d13h
12factor-app-a-deployment-7c5c8db577-jzxjt   2/2     Running   0          4d13h
12factor-app-b-deployment-649f7f7c78-fnlkh   2/2     Running   0          6d
12factor-app-b-deployment-649f7f7c78-tbtjx   2/2     Running   0          6d

```

Test your microservices by hitting the following url
http://localhost:30080

You should see the welcome page and each link should work.
Hope you have enjoyed the journey towards 12 Factor App!