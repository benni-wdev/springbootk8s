# springbootk8s
Simple springboot webapp with gradle, docker, jenkins and kubernetes deployment to show the interlinks between docker, jenkins and kubernets.

# Before it works
Please replace your.local.registry:5000 with the ip and port of your local docker registry in Jenkinsfile and k8s/deployment.yaml.
For setting up a local docker registry please check 

Your jenkins need to have access to kubectl with correct config to access your cluster


--------------------------------------
benni-wdev

[https://www.wdev.ch](https://www.wdev.ch/)