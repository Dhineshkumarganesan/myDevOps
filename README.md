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

*****************************************************
CKS - Certified Kubernetes Security Lab
*************************************
*****************************************************
Lab - Run CIS Benchmark Assessment tool on Ubuntu
*************************************************
1
**What is CIS**

Center for Internet Security

2
**What is not a function of CIS?**

Monitor global internet activities

3
**We have installed the CIS-CAT Pro Assessor tool called Assessor-CLI, under /root.**

Please run the assessment with the Assessor-CLI.sh script inside Assessor directory and generate a report called index.html in the output directory /var/www/html/.Once done, the report can be viewed using the Assessment Report tab located above the terminal.

Run the test in interactive mode and use below settings:

Benchmarks/Data-Stream Collections: : CIS Ubuntu Linux 20.04 LTS Benchmark v2.0.1

Profile : Level 1 - Server

cd /root/Assessor
sh ./Assessor-CLI.sh -i -rd /var/www/html/ -nts -rp index

Benchmarks/Data-Stream Collections: CIS Ubuntu Linux 20.04 LTS Benchmark v2.0.1

Profile: Level 1 - Server

Below the Assessment Result Summary


-----------------------------------------------------------------------------
 ***** Assessment Results Summary *****
-----------------------------------------------------------------------------
   Total # of Results: 285
 Total Scored Results: 206
           Total Pass: 121
           Total Fail: 85
          Total Error: 0
        Total Unknown: 0
 Total Not Applicable: 0
    Total Not Checked: 15
   Total Not Selected: 56
  Total Informational: 8
-----------------------------------------------------------------------------
 ***** Assessment Scoring *****
-----------------------------------------------------------------------------
         Score Earned: 121.0
    Maximum Available: 206.0
                Total: 58.74%
-----------------------------------------------------------------------------

- Generating Checklist Results...

Ending Assessment - Date & Time: 04-19-2025 11:49:33
Total Assessment Time: 30 seconds
- Generating Asset Reporting Format.
  - Generating Report Request.
- Generating Data-Stream Collection.
- Data-Stream Collection Generated.
  - Collecting Checklist Results.
  - Combining Results.
  - Saving Results.
- Asset Reporting Format Generated.

 ***** Writing Assessment Results ***** 
 - Reports saving to /var/www/html
 -- index.html
Assessment Complete for Checklist: CIS Ubuntu Linux 20.04 LTS Benchmark
-----------------------------------------------------------
Disconnecting Session.
Finished Assessment 1/1
Exiting; Exit Code: 0

![image](https://github.com/user-attachments/assets/6937bc69-33a4-41a1-a649-95f6eb596012)



*****************************************************
Lab - Kube-bench
*************************************************
Run the kube-bench test again and ensure that all tests 

./kube-bench --config-dir `pwd`/cfg --config `pwd`/cfg/config.yaml
