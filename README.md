# sample-app-node
Deploy NodeJS Application
1. Go to the sample node app repo root directory, Deploy the manifest by running the following command:


$ kubectl apply -f deployment/
 It will create app pod and web service.


2. Generate request from inside the app pod or from your terminal if you can access web service loadbalancer endpoint.


$ kubectl exec -it <app pod> -- curl localhost:8080/hello
 
$ kubectl exec -it <app pod> -- curl localhost:8080/hi
 
$ kubectl exec -it <app pod> -- curl localhost:8080/error
 
$ kubectl exec -it <app pod> -- curl localhost:8080/warn

e.g. kubectl exec -it nodejs-598d4f59c5-kfxnj -- curl localhost:8080/hello
