# myDevOps



 Here are some daily useful commands for DevOps:
 hashtag#Linux_Commands:-
 1. Check server uptime: “uptime”
 2. Check disk usage: `df -h`
 3. Check memory usage: `free -m`
 4. Check CPU usage: `top` or `htop`
 5. Check logs: `tail -f /var/log/syslog`
 6. Check network connections: `netstat -tlnp`
 7. Check running processes: `ps aux`
 8. Kill a process: `kill <pid>`
 9. Check file permissions: `ls -l`
 10.Change file permissions: `chmod <permissions> <file>`
 
 hashtag#Docker_Commands:-
 1. List running containers: `docker ps`
 2. Start a container: `docker start <container_name>`
 3. Stop a container: `docker stop <container_name>`
 4. Remove a container: `docker rm <container_name>`
 5. List all containers: `docker ps -a`
 6. Pull an image: `docker pull <image_name>`
 7. Run a container: `docker run -d <image_name>`
 8. Exec into a container: `docker exec -it <container_name> /bin/bash`
 9. Check container logs: `docker logs <container_name>`
 10.Build a Docker image: `docker build -t <image_name> .`
 
 hashtag#Kubernetes_Commands:-
 1. Get nodes: `kubectl get nodes`
 2. Get pods: `kubectl get pods`
 3. Get deployments: `kubectl get deployments`
 4. Get services: `kubectl get svc`
 5. Create a deployment: `kubectl create deployment <deployment_name> --image=<image_name>`
 6. Apply a configuration: `kubectl apply -f <config_file>`
 7. Get pod logs: `kubectl logs <pod_name>`
 8. Exec into a pod: `kubectl exec -it <pod_name> -- /bin/bash`
 9. Scale a deployment: `kubectl scale deployment <deployment_name> --replicas=<replica_count>`
 10.Delete a po: `kubectl delete pod <pod_name>`


 
 hashtag#Git_Commands:-
 1. Clone a repository: `git clone <repository_url>`
 2. Check repository status: `git status`
 3. Add changes: `git add <file_name>`
 4. Commit changes: `git commit -m "<commit_message>"`
 5. Push changes: `git push <remote_name> <branch_name>`
 6. Pull changes: `git pull <remote_name> <branch_name>`
 7. Check commit history: `git log`
 8. Create a new branch: `git branch <branch_name>`
 9. Switch to a branch: `git checkout <branch_name>`
 10.Merge a branch: `git merge <branch_name>`
 
 hashtag#AWS_Commands:-
 1. List EC2 instances: `aws ec2 describe-instances`
 2. Create an EC2 instance: `aws ec2 run-instances --image-id <image_id> --instance-type <instance_type>`
 3. Start an EC2 instance


CKS
*************************************

Run the kube-bench test again and ensure that all tests 

./kube-bench --config-dir `pwd`/cfg --config `pwd`/cfg/config.yaml
