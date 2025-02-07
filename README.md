# Redhat Rhelai Ansible Project

Simple RHEL AI setup using Ansible on AWS.

## Getting started
Install the collections specified under `collections/requirements.yml`
```
ansible-galaxy collection install -r collections/requirements.yml
```

## Set the Role variables

Checkout the `sample_vars.yml` file in project root.

Ensure correct variables are set before running the playbook `awsrhelai.yml`

## Run the playbook

```
ansible-playbook awsrhelai.yml -e @sample_vars.yml
```

## Testing the model via CLI
You can ssh into the system with the private key created and run the command below
```
ilab model chat -m ~/.cache/instructlab/models/granite-8b-starter-v1 --endpoint-url http://0.0.0.0:8000/v1 --api-key demotoken
```

```
>>> Tell me how cool is Ansible?   
Ansible is a powerful, agentless automation and configuration management tool that simplifies the process of managing and deploying infrastructure resources. It is often referred to as "infrastructure as code" and enables organizations to automate repetitive tasks, reduce errors, and accelerate the deployment and configuration of servers, applications, and services.

Ansible is highly popular due to its simplicity and ease of use. It uses a human-readable language called YAML (Yet Another Markup Language) to define the tasks and configurations that need to be executed. This makes it easy for both beginners and experienced users to create and manage Ansible playbooks, which are collections of commands and tasks that can be executed on multiple servers simultaneously.

Another reason why Ansible is so cool is that it does not require any agents to be installed on the target servers. This means that Ansible can be used to manage and configure servers that are running a wide range of operating systems, including Linux, Windows, and macOS. It also reduces the overhead associated with managing agents and ensures that the infrastructure is as secure as possible.

Ansible also supports a wide range of plugins and modules, which can be used to integrate it with other tools and services. For example, it can be used to manage and configure cloud infrastructure, container orchestration platforms, and DevOps tools.

In summary, Ansible is a powerful and versatile tool that enables organizations to automate and manage their infrastructure resources efficiently and effectively. Its simplicity, ease of use, and agentless architecture make it a popular choice among DevOps professionals and infrastructure teams.
```

### HAPPY AUTOMATING ###
