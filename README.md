# Docker Swarm Project
This practice is about deploying a Tomcat stack using docker swarm. Here are the steps:

## Step 01:
Initialize Docker Swarm on the master node:
```bash
docker swarm init
```
It will output a join command for worker node.

## Step 02:
Join the worker node to the swarm cluster
```bash
docker swarm join --token required-token required-ipaddress:port
```

## Step 03:
Check if the node(s) have successfully joined the cluster:
```bash
docker node ls
```

## Step 04:
Deploy the Tomcat stack on the cluster:
```bash
docker stack deploy -c stack.yaml tomcat_stack
```

## Step 05:
Check the status of cluster:
```bash
docker stack services tomcat_stack
docker stack ps tomcat_stack
```
