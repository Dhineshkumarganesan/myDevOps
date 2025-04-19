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

- Evaluating Checklist Rules
01/285: Ensure mounting of cramfs filesystems is disabled........................................... Pass
02/285: Ensure mounting of freevxfs filesystems is disabled......................................... Pass
03/285: Ensure mounting of jffs2 filesystems is disabled............................................ Pass
04/285: Ensure mounting of hfs filesystems is disabled.............................................. Pass
05/285: Ensure mounting of hfsplus filesystems is disabled.......................................... Pass
06/285: Ensure mounting of squashfs filesystems is disabled......................................... Not Selected
07/285: Ensure mounting of udf filesystems is disabled.............................................. Not Selected
08/285: Ensure /tmp is a separate partition......................................................... Fail
09/285: Ensure nodev option set on /tmp partition................................................... Pass
10/285: Ensure noexec option set on /tmp partition.................................................. Pass
11/285: Ensure nosuid option set on /tmp partition.................................................. Pass
12/285: Ensure separate partition exists for /var................................................... Not Selected
13/285: Ensure nodev option set on /var partition................................................... Pass
14/285: Ensure nosuid option set on /var partition.................................................. Pass
15/285: Ensure separate partition exists for /var/tmp............................................... Not Selected
16/285: Ensure nodev option set on /var/tmp partition............................................... Pass
17/285: Ensure noexec option set on /var/tmp partition.............................................. Pass
18/285: Ensure nosuid option set on /var/tmp partition.............................................. Pass
19/285: Ensure separate partition exists for /var/log............................................... Not Selected
20/285: Ensure nodev option set on /var/log partition............................................... Pass
21/285: Ensure noexec option set on /var/log partition.............................................. Pass
22/285: Ensure nosuid option set on /var/log partition.............................................. Pass
23/285: Ensure separate partition exists for /var/log/audit......................................... Not Selected
24/285: Ensure nodev option set on /var/log/audit partition......................................... Pass
25/285: Ensure noexec option set on /var/log/audit partition........................................ Pass
26/285: Ensure nosuid option set on /var/log/audit partition........................................ Pass
27/285: Ensure separate partition exists for /home.................................................. Not Selected
28/285: Ensure nodev option set on /home partition.................................................. Pass
29/285: Ensure nosuid option set on /home partition................................................. Pass
30/285: Ensure nodev option set on /dev/shm partition............................................... Pass
31/285: Ensure noexec option set on /dev/shm partition.............................................. Pass
32/285: Ensure nosuid option set on /dev/shm partition.............................................. Pass
33/285: Disable Automounting........................................................................ Pass
34/285: Disable USB Storage......................................................................... Fail
35/285: Ensure AIDE is installed.................................................................... Fail
36/285: Ensure filesystem integrity is regularly checked............................................ Fail
37/285: Ensure updates, patches, and additional security software are installed..................... Not Checked
38/285: Ensure package manager repositories are configured.......................................... Not Checked
39/285: Ensure GPG keys are configured.............................................................. Not Checked
40/285: Ensure bootloader password is set........................................................... Fail
41/285: Ensure permissions on bootloader config are configured...................................... Fail
42/285: Ensure authentication required for single user mode......................................... Pass
43/285: Ensure prelink is not installed............................................................. Pass
44/285: Ensure address space layout randomization (ASLR) is enabled................................. Fail
45/285: Ensure ptrace_scope is restricted........................................................... Pass
46/285: Ensure Automatic Error Reporting is not enabled............................................. Pass
47/285: Ensure core dumps are restricted............................................................ Fail
48/285: Ensure AppArmor is installed................................................................ Fail
49/285: Ensure AppArmor is enabled in the bootloader configuration.................................. Fail
50/285: Ensure all AppArmor Profiles are in enforce or complain mode................................ Fail
51/285: Ensure all AppArmor Profiles are enforcing.................................................. Not Selected
52/285: Ensure message of the day is configured properly............................................ Pass
53/285: Ensure local login warning banner is configured properly.................................... Fail
54/285: Ensure remote login warning banner is configured properly................................... Fail
55/285: Ensure permissions on /etc/motd are configured.............................................. Pass
56/285: Ensure permissions on /etc/issue are configured............................................. Pass
57/285: Ensure permissions on /etc/issue.net are configured......................................... Pass
58/285: Ensure GNOME Display Manager is removed..................................................... Not Selected
59/285: Ensure GDM login banner is configured....................................................... Pass
60/285: Ensure GDM disable-user-list option is enabled.............................................. Pass
61/285: Ensure GDM screen locks when the user is idle............................................... Pass
62/285: Ensure GDM screen locks cannot be overridden................................................ Pass
63/285: Ensure GDM automatic mounting of removable media is disabled................................ Pass
64/285: Ensure GDM disabling automatic mounting of removable media is not overridden................ Pass
65/285: Ensure GDM autorun-never is enabled......................................................... Pass
66/285: Ensure GDM autorun-never is not overridden.................................................. Pass
67/285: Ensure XDCMP is not enabled................................................................. Pass
68/285: Ensure a single time synchronization daemon is in use....................................... Pass
69/285: Ensure chrony is configured with authorized timeserver...................................... Informational
70/285: Ensure chrony is running as user _chrony.................................................... Pass
71/285: Ensure chrony is enabled and running........................................................ Pass
72/285: Ensure systemd-timesyncd configured with authorized timeserver.............................. Fail
73/285: Ensure systemd-timesyncd is enabled and running............................................. Informational
74/285: Ensure ntp access control is configured..................................................... Pass
75/285: Ensure ntp is configured with authorized timeserver......................................... Informational
76/285: Ensure ntp is running as user ntp........................................................... Pass
77/285: Ensure ntp is enabled and running........................................................... Pass
78/285: Ensure X Window System is not installed..................................................... Not Selected
79/285: Ensure Avahi Server is not installed........................................................ Pass
80/285: Ensure CUPS is not installed................................................................ Pass
81/285: Ensure DHCP Server is not installed......................................................... Pass
82/285: Ensure LDAP server is not installed......................................................... Pass
83/285: Ensure NFS is not installed................................................................. Pass
84/285: Ensure DNS Server is not installed.......................................................... Pass
85/285: Ensure FTP Server is not installed.......................................................... Pass
86/285: Ensure HTTP server is not installed......................................................... Fail
87/285: Ensure IMAP and POP3 server are not installed............................................... Pass
88/285: Ensure Samba is not installed............................................................... Pass
89/285: Ensure HTTP Proxy Server is not installed................................................... Pass
90/285: Ensure SNMP Server is not installed......................................................... Pass
91/285: Ensure NIS Server is not installed.......................................................... Pass
92/285: Ensure dnsmasq is not installed............................................................. Pass
93/285: Ensure mail transfer agent is configured for local-only mode................................ Pass
94/285: Ensure rsync service is either not installed or is masked................................... Pass
95/285: Ensure NIS Client is not installed.......................................................... Pass
96/285: Ensure rsh client is not installed.......................................................... Pass
97/285: Ensure talk client is not installed......................................................... Pass
98/285: Ensure telnet client is not installed....................................................... Fail
99/285: Ensure LDAP client is not installed......................................................... Pass
100/285: Ensure  RPC is not installed............................................................... Pass
101/285: Ensure nonessential services are removed or masked......................................... Not Checked
102/285: Ensure IPv6 status is identified........................................................... Informational
103/285: Ensure wireless interfaces are disabled.................................................... Pass
104/285: Ensure bluetooth is disabled............................................................... Pass
105/285: Ensure DCCP is disabled.................................................................... Not Selected
106/285: Ensure SCTP is disabled.................................................................... Not Selected
107/285: Ensure RDS is disabled..................................................................... Not Selected
108/285: Ensure TIPC is disabled.................................................................... Not Selected
109/285: Ensure packet redirect sending is disabled................................................. Fail
110/285: Ensure IP forwarding is disabled........................................................... Fail
111/285: Ensure source routed packets are not accepted.............................................. Fail
112/285: Ensure ICMP redirects are not accepted..................................................... Fail
113/285: Ensure secure ICMP redirects are not accepted.............................................. Fail
114/285: Ensure suspicious packets are logged....................................................... Fail
115/285: Ensure broadcast ICMP requests are ignored................................................. Fail
116/285: Ensure bogus ICMP responses are ignored.................................................... Fail
117/285: Ensure Reverse Path Filtering is enabled................................................... Fail
118/285: Ensure TCP SYN Cookies is enabled.......................................................... Fail
119/285: Ensure IPv6 router advertisements are not accepted......................................... Fail
120/285: Ensure ufw is installed.................................................................... Fail
121/285: Ensure iptables-persistent is not installed with ufw....................................... Pass
122/285: Ensure ufw service is enabled.............................................................. Fail
123/285: Ensure ufw loopback traffic is configured.................................................. Fail
124/285: Ensure ufw outbound connections are configured............................................. Not Checked
125/285: Ensure ufw firewall rules exist for all open ports......................................... Fail
126/285: Ensure ufw default deny firewall policy.................................................... Fail
127/285: Ensure nftables is installed............................................................... Fail
128/285: Ensure ufw is uninstalled or disabled with nftables........................................ Pass
129/285: Ensure iptables are flushed with nftables.................................................. Not Checked
130/285: Ensure a nftables table exists............................................................. Fail
131/285: Ensure nftables base chains exist.......................................................... Fail
132/285: Ensure nftables loopback traffic is configured............................................. Fail
133/285: Ensure nftables outbound and established connections are configured........................ Not Checked
134/285: Ensure nftables default deny firewall policy............................................... Fail
135/285: Ensure nftables service is enabled......................................................... Fail
136/285: Ensure nftables rules are permanent........................................................ Fail
137/285: Ensure iptables packages are installed..................................................... Fail
138/285: Ensure nftables is not installed with iptables............................................. Pass
139/285: Ensure ufw is uninstalled or disabled with iptables........................................ Pass
140/285: Ensure iptables default deny firewall policy............................................... Fail
141/285: Ensure iptables loopback traffic is configured............................................. Fail
142/285: Ensure iptables outbound and established connections are configured........................ Not Checked
143/285: Ensure iptables firewall rules exist for all open ports.................................... Fail
144/285: Ensure ip6tables default deny firewall policy.............................................. Fail
145/285: Ensure ip6tables loopback traffic is configured............................................ Fail
146/285: Ensure ip6tables outbound and established connections are configured....................... Not Checked
147/285: Ensure ip6tables firewall rules exist for all open ports................................... Fail
148/285: Ensure cron daemon is enabled and active................................................... Pass
149/285: Ensure permissions on /etc/crontab are configured.......................................... Fail
150/285: Ensure permissions on /etc/cron.hourly are configured...................................... Fail
151/285: Ensure permissions on /etc/cron.daily are configured....................................... Fail
152/285: Ensure permissions on /etc/cron.weekly are configured...................................... Fail
153/285: Ensure permissions on /etc/cron.monthly are configured..................................... Fail
154/285: Ensure permissions on /etc/cron.d are configured........................................... Fail
155/285: Ensure cron is restricted to authorized users.............................................. Fail
156/285: Ensure at is restricted to authorized users................................................ Pass
157/285: Ensure permissions on /etc/ssh/sshd_config are configured.................................. Fail
158/285: Ensure permissions on SSH private host key files are configured............................ Pass
159/285: Ensure permissions on SSH public host key files are configured............................. Pass
160/285: Ensure SSH access is limited............................................................... Fail
161/285: Ensure SSH LogLevel is appropriate......................................................... Pass
162/285: Ensure SSH PAM is enabled.................................................................. Pass
163/285: Ensure SSH root login is disabled.......................................................... Fail
164/285: Ensure SSH HostbasedAuthentication is disabled............................................. Pass
165/285: Ensure SSH PermitEmptyPasswords is disabled................................................ Pass
166/285: Ensure SSH PermitUserEnvironment is disabled............................................... Pass
167/285: Ensure SSH IgnoreRhosts is enabled......................................................... Pass
168/285: Ensure SSH X11 forwarding is disabled...................................................... Not Selected
169/285: Ensure only strong Ciphers are used........................................................ Pass
170/285: Ensure only strong MAC algorithms are used................................................. Fail
171/285: Ensure only strong Key Exchange algorithms are used........................................ Pass
172/285: Ensure SSH AllowTcpForwarding is disabled.................................................. Not Selected
173/285: Ensure SSH warning banner is configured.................................................... Pass
174/285: Ensure SSH MaxAuthTries is set to 4 or less................................................ Fail
175/285: Ensure SSH MaxStartups is configured....................................................... Fail
176/285: Ensure SSH LoginGraceTime is set to one minute or less..................................... Fail
177/285: Ensure SSH MaxSessions is set to 10 or less................................................ Pass
178/285: Ensure SSH Idle Timeout Interval is configured............................................. Pass
179/285: Ensure sudo is installed................................................................... Pass
180/285: Ensure sudo commands use pty............................................................... Fail
181/285: Ensure sudo log file exists................................................................ Fail
182/285: Ensure users must provide password for privilege escalation................................ Not Selected
183/285: Ensure re-authentication for privilege escalation is not disabled globally................. Pass
184/285: Ensure sudo authentication timeout is configured correctly................................. Pass
185/285: Ensure access to the su command is restricted.............................................. Fail
186/285: Ensure password creation requirements are configured....................................... Fail
187/285: Ensure lockout for failed password attempts is configured.................................. Fail
188/285: Ensure password reuse is limited........................................................... Fail
189/285: Ensure strong password hashing algorithm is configured..................................... Pass
190/285: Ensure all current passwords uses the configured hashing algorithm......................... Not Checked
191/285: Ensure minimum days between password changes is  configured................................ Fail
192/285: Ensure password expiration is 365 days or less............................................. Fail
193/285: Ensure password expiration warning days is 7 or more....................................... Pass
194/285: Ensure inactive password lock is 30 days or less........................................... Fail
195/285: Ensure all users last password change date is in the past.................................. Pass
196/285: Ensure the number of changed characters in a new password is configured.................... Fail
197/285: Ensure preventing the use of dictionary words for passwords is configured.................. Fail
198/285: Ensure system accounts are secured......................................................... Pass
199/285: Ensure default group for the root account is GID 0......................................... Pass
200/285: Ensure default user umask is 027 or more restrictive....................................... Fail
201/285: Ensure default user shell timeout is configured............................................ Fail
202/285: Ensure nologin is not listed in /etc/shells................................................ Not Selected
203/285: Ensure maximum number of same consecutive characters in a password is configured........... Fail
204/285: Ensure systemd-journal-remote is installed................................................. Fail
205/285: Ensure systemd-journal-remote is configured................................................ Not Checked
206/285: Ensure systemd-journal-remote is enabled................................................... Informational
207/285: Ensure journald is not configured to receive logs from a remote client..................... Pass
208/285: Ensure journald service is enabled......................................................... Pass
209/285: Ensure journald is configured to compress large log files.................................. Fail
210/285: Ensure journald is configured to write logfiles to persistent disk......................... Fail
211/285: Ensure journald is not configured to send logs to rsyslog.................................. Informational
212/285: Ensure journald log rotation is configured per site policy................................. Not Checked
213/285: Ensure journald default file permissions configured........................................ Not Checked
214/285: Ensure rsyslog is installed................................................................ Fail
215/285: Ensure rsyslog service is enabled.......................................................... Fail
216/285: Ensure journald is configured to send logs to rsyslog...................................... Informational
217/285: Ensure rsyslog default file permissions are configured..................................... Fail
218/285: Ensure logging is configured............................................................... Not Checked
219/285: Ensure rsyslog is configured to send logs to a remote log host............................. Informational
220/285: Ensure rsyslog is not configured to receive logs from a remote client...................... Pass
221/285: Ensure all logfiles have appropriate access configured..................................... Pass
222/285: Ensure auditd is installed................................................................. Not Selected
223/285: Ensure auditd service is enabled and active................................................ Not Selected
224/285: Ensure auditing for processes that start prior to auditd is enabled........................ Not Selected
225/285: Ensure audit_backlog_limit is sufficient................................................... Not Selected
226/285: Ensure audit log storage size is configured................................................ Not Selected
227/285: Ensure audit logs are not automatically deleted............................................ Not Selected
228/285: Ensure system is disabled when audit logs are full......................................... Not Selected
229/285: Ensure changes to system administration scope (sudoers) is collected....................... Not Selected
230/285: Ensure actions as another user are always logged........................................... Not Selected
231/285: Ensure events that modify the sudo log file are collected.................................. Not Selected
232/285: Ensure events that modify date and time information are collected.......................... Not Selected
233/285: Ensure events that modify the system's network environment are collected................... Not Selected
234/285: Ensure use of privileged commands are collected............................................ Not Selected
235/285: Ensure unsuccessful file access attempts are collected..................................... Not Selected
236/285: Ensure events that modify user/group information are collected............................. Not Selected
237/285: Ensure discretionary access control permission modification events are collected........... Not Selected
238/285: Ensure successful file system mounts are collected......................................... Not Selected
239/285: Ensure session initiation information is collected......................................... Not Selected
240/285: Ensure login and logout events are collected............................................... Not Selected
241/285: Ensure file deletion events by users are collected......................................... Not Selected
242/285: Ensure events that modify the system's Mandatory Access Controls are collected............. Not Selected
243/285: Ensure successful and unsuccessful attempts to use the chcon command are recorded.......... Not Selected
244/285: Ensure successful and unsuccessful attempts to use the setfacl command are recorded........ Not Selected
245/285: Ensure successful and unsuccessful attempts to use the chacl command are recorded.......... Not Selected
246/285: Ensure successful and unsuccessful attempts to use the usermod command are recorded........ Not Selected
247/285: Ensure kernel module loading unloading and modification is collected....................... Not Selected
248/285: Ensure the audit configuration is immutable................................................ Not Selected
249/285: Ensure the running and on disk configuration is the same................................... Not Selected
250/285: Ensure audit log files are mode 0640 or less permissive.................................... Not Selected
251/285: Ensure only authorized users own audit log files........................................... Not Selected
252/285: Ensure only authorized groups are assigned ownership of audit log files.................... Not Selected
253/285: Ensure the audit log directory is 0750 or more restrictive................................. Not Selected
254/285: Ensure audit configuration files are 640 or more restrictive............................... Not Selected
255/285: Ensure audit configuration files are owned by root......................................... Not Selected
256/285: Ensure audit configuration files belong to group root...................................... Not Selected
257/285: Ensure audit tools are 755 or more restrictive............................................. Not Selected
258/285: Ensure audit tools are owned by root....................................................... Not Selected
259/285: Ensure audit tools belong to group root.................................................... Not Selected
260/285: Ensure cryptographic mechanisms are used to protect the integrity of audit tools........... Fail
261/285: Ensure permissions on /etc/passwd are configured........................................... Pass
262/285: Ensure permissions on /etc/passwd- are configured.......................................... Pass
263/285: Ensure permissions on /etc/group are configured............................................ Pass
264/285: Ensure permissions on /etc/group- are configured........................................... Pass
265/285: Ensure permissions on /etc/shadow are configured........................................... Pass
266/285: Ensure permissions on /etc/shadow- are configured.......................................... Pass
267/285: Ensure permissions on /etc/gshadow are configured.......................................... Pass
268/285: Ensure permissions on /etc/gshadow- are configured......................................... Pass
269/285: Ensure permissions on /etc/shells are configured........................................... Pass
270/285: Ensure permissions on /etc/opasswd are configured.......................................... Fail
271/285: Ensure world writable files and directories are secured.................................... Fail
272/285: Ensure no unowned or ungrouped files or directories exist.................................. Pass
273/285: Ensure SUID and SGID files are reviewed.................................................... Not Checked
274/285: Ensure accounts in /etc/passwd use shadowed passwords...................................... Pass
275/285: Ensure /etc/shadow password fields are not empty........................................... Pass
276/285: Ensure all groups in /etc/passwd exist in /etc/group....................................... Pass
277/285: Ensure shadow group is empty............................................................... Pass
278/285: Ensure no duplicate UIDs exist............................................................. Pass
279/285: Ensure no duplicate GIDs exist............................................................. Pass
280/285: Ensure no duplicate user names exist....................................................... Pass
281/285: Ensure no duplicate group names exist...................................................... Pass
282/285: Ensure root PATH Integrity................................................................. Pass
283/285: Ensure root is the only UID 0 account...................................................... Pass
284/285: Ensure local interactive user home directories are configured.............................. Fail
285/285: Ensure local interactive user dot files access is configured............................... Fail

5


6


7



8

**Fix the failed test - 5.1.2.1 Ensure rsyslog is installed**

Note: If the packages are not available, run the apt update command to refresh the package list before proceeding.

Follow exact commands given in Remediation of given test

Run the command **apt install rsyslog** to install rsyslog


9
Fix the failed test **- 4.1.2 Ensure permissions on /etc/crontab** are configured

To ensure the permissions on /etc/crontab are configured correctly, you need to set the appropriate permissions and ownership. According to the CIS benchmark, the file should have the following settings:

Permissions: 644 (read and write for owner, read for group and others)
Owner: root
Group: root
Here's how you can achieve this:

Set the correct permissions:
   **chmod 644 /etc/crontab**

Set the correct ownership:
   **chown root:root /etc/crontab**

After making these changes, you can verify them by running:

**stat -c "%A %U %G" /etc/crontab**

This command should output:

**-rw-r--r-- root root**

This indicates that the permissions and ownership are set correctly. Let me know if you need further assistance! 😊


![image](https://github.com/user-attachments/assets/8909877c-b9d6-4173-b4e1-98bad8c17cbd)


10
In the previous questions we fixed the below 3 failed tests. Now run CIS-CAT tool test again and verify that all the below tests pass.

- 1.7.2 Ensure local login warning banner is configured properly

- 5.1.2.1 Ensure rsyslog is installed

- 4.1.2 Ensure permissions on /etc/crontab are configured

Run below command again to confirm that tests are passing now!

**sh ./Assessor-CLI.sh -i -rd /var/www/html/ -nts -rp index**

Use below setting while running tests!

Benchmarks/Data-Stream Collections: CIS Ubuntu Linux 20.04 LTS Benchmark v2.0.1

Profile: Level 1 - Server

![image](https://github.com/user-attachments/assets/611d6398-f7f3-453f-b814-f234366ae891)

![image](https://github.com/user-attachments/assets/5b8d18dc-91c5-4e84-ae4c-c7a7c32090bb)

![image](https://github.com/user-attachments/assets/a1c09274-a716-4dde-a1bf-22031a6aeec3)




*****************************************************
Lab - Kube-bench
*************************************************
Run the kube-bench test again and ensure that all tests 

./kube-bench --config-dir `pwd`/cfg --config `pwd`/cfg/config.yaml
