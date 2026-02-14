# ansible_semaphore_homeserver
jenkins-ansible-semaphore-cicd

```text
jenkins-ansible-semaphore-cicd/
│
├── Jenkinsfile
├── README.md
├── docs/
│   ├── architecture.png
│   └── setup-guide.md
├── screenshots/
│   ├── pipeline-success.png
│   └── semaphore-run.png
└── ansible/
    └── playbooks/
```


# Jenkins -> Semaphore CI/CD Integration (HomeServer)

# Architecture 

GitHub -> Jenkins -> Semaphore -> Ansible -> Target Host

# Environment 

- Ubuntu Server 24.04
- Jenkins (Docker)
- Ansible (Semaphore UI)
- Docker Network

# Secure API Integration 
Jenkins securely triggers Semaphore deployment using API token stored in Jenkins Credientials 

Endpoint used:

POST /api/project/1/tasks
Body:
{
  "template_id": 1
}

## Pipeline Stages 

1. Testing Stage
2. Deployment Trigger Stage

## Successful Deployment Response 
<img width="1895" height="649" alt="image" src="https://github.com/user-attachments/assets/543aeb3d-00e3-4877-a923-beabe72202be" />

HTTP 201 Created 

<img width="1366" height="816" alt="image" src="https://github.com/user-attachments/assets/0f7b9018-8686-44e2-8398-b740a056cdac" />
<img width="1362" height="698" alt="image" src="https://github.com/user-attachments/assets/c33eda7f-87a9-4539-9740-e71a5cdb2fed" />





