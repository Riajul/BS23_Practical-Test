# App 1 Image Build and Deploy in Cluster with YAML

** Image Build and Push to Repo
>docker build -t mizapp1 .
>docker tag mizapp1:latest dockerhubrepo:tag
>docker push dockerhubrepo:tag

Make sure Dockerfile and app src file is in same folder.

**Node Selection
To select the node selector we need to label the nodes

>kubectl label nodes hostname app1-deploy=true --overwrite

**Image Deploy
Here we have used jenkinsfile , so create a Pipeline project and set definition "Pipeline Script From SCM"
set your Repo URL and Script Path "JenkinsFile"
If your repo is public, so no need for 'Credentials.'

If you don't use jenkins, you can deploy Like that after logging to Kubernetes Server.

>kubectl apply -f BrainStationTest/Task1/app1/deploy/app1deploy.yaml
>kubectl apply -f BrainStationTest/Task1/app1/deploy/app1service.yaml

As there is no DB/redis server,,just a normal app so there is no config.yaml