# Redhat Rhelai Ansible Project

Simple RHEL AI setup using Ansible on AWS.

## Getting started
Install the collections specified under `collections/requirements.yml`
```
ansible-galaxy collection install -r collections/requirements.yml
```

## Set the Role variables

Checkout the `sample_vars.yml` file in project root
Ensure correct variables are set before running the playbook `awsrhelai.yml`

## Run the playbook

```
ansible-playbook awsrhelai.yml -e @sample_vars.yml
```

### HAPPY AUTOMATING ###
