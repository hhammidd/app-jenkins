# Steps of deployment
## App buid part
0. Check you have docker and kubernetes up/running 
    * Kubectl is installed
    * docker installed
        * docker desktop
        * docker hub
    * kubernetes: 
        * minikube
        * docker desktop
        * google
        * Azur
        
1. create a finalName for app <app-name>
2. Create a new version of app or change it
3. Create a build : `mvn clean install` >> Artifactory

## Image and docker part
4. Check docker images : `docker image ls`
5. Create a `Dockerfile` to generate app image : 
```
FROM openjdk:8
EXPOSE 8070
ADD target/docker-jenkins.jar docker-jenkins.jar
ENTRYPOINT ["java","-jar","/docker-jenkins.jar"]
``` 
6. Build an image from Dockerfile with version :`docker build -f Dockerfile -t <app-name>:<app-version> .`
    * check image exist : `docker image ls`
    * Check image is correct before deploy to kubernetes by build container: `docker run -p <port>:<port> <app-name>`
    * stop container :`docker container stop $(docker container ls -aq)`

## Kubernetes and deployment part
7. Check the kubernetes objects:
    * Check which is kubernetes provider : `kubectl config get-contexts`
        * Possible: minikube, google-cloud/aws/azur/docker-desktop
        * switch with : `k config use-context docker-for-desktop`
    * nodes will be ready : `kubectl get nodes -o wide`
    * Pods: `k get pods` , in case of no pods:
        ```
        No resources found in default namespace.
        ```    
    * Replication: `k get rc`
    * Service: `k get svc`
    * Deploy: `k get deploy`
8. In case everything is clean , create a service `svc.yml`:
    * create file :
    ```
    apiVersion: v1
    kind: Service
    metadata:
      name: hello-svc
      labels:
        app: docker-jenkins
    spec:
      type: NodePort
      ports:
      - port: 8070
        nodePort: 30001
        protocol: TCP
      selector:
        app: docker-jenkins
    ``` 
    * Create it in k8s: `k create -f svc.yml`
9. create a deploy with the same version as image:
    * Create `deploy.yml`:
    ```
    apiVersion: apps/v1
    kind: Deployment
    metadata:
      name: hello-deploy
    spec:
      selector:
        matchLabels:
          app: docker-jenkins
      replicas: 2
      minReadySeconds: 10
      strategy:
        type: RollingUpdate
        rollingUpdate:
          maxUnavailable: 1
          maxSurge: 1
      template:
          metadata:
            labels:
              app: docker-jenkins
          spec:
            containers:
            - name: docker-jenkins
              image: docker-jenkins:v5
              ports:
              - containerPort: 8070
    ```    
    * Create deploy in kubernetes: `k create -f deploy.yml`
    * See that deploy is Available and UP/RUNNING:
     ```
     ➜  app-jenkins git:(master) ✗ k get deploy
     NAME           READY   UP-TO-DATE   AVAILABLE   AGE
     hello-deploy   2/2     2            2           37s
     ```
* Go to the: `localhost:30001/lazy`
* Hoooray
    