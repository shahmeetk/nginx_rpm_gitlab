##  NGINX Building with GITLAB CI Ansible and Docker Compose ###

### Task 1: Create Dockerfile to Build OpenSource GitLab and Attach Runner

Created Docker Compose file containing :
```
    - web
    - gitlab-runner
```

Docker Images:
```
GitLab Opensouce: gitlab/gitlab-ce:latest
Configure Runner: gitlab/gitlab-runner:latest
```
### Task 2: Pipeline with NGINX Build Jobs:

Configuration File: **_gitlab-ci.yml_**
```
JOB1 : Build NGINX with latest RPM

JOB2 : sign RPM with GCP Key
```

### Task 3: Ansible Playbook to Build created NGINX on Server with SSL Configuration

Configuration File: **_ansible_playbook.yml_**

```
1. Copy Nginx RPM Package to Host
2. Install Copied Nginx Package
3. Configure Self SSL Termination with nginx.conf.j2
4. Restart the Nginx
```