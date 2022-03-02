# Instruction to Run Nginx Container

1. To deploy the configmap
>kubectl apply -f nginxconfig.yaml

2. To deploy the Pod of nginx
>kubectl apply -f nginx.yaml

3. Last deploy the service of nginx
>kubectl apply -f nginxservice.yaml