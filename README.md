# ansible-vsts-agent-deploy
## Introduction
Ansible deployment of VSTS Agent to CoreOS in Azure using containers.

## Information
Shouldn't be run as release in VSTS / Azure DevOps, since it creates the agents which release pipeline uses.

## How to run
```bash
ansible-playbook -i hosts-prd site.yml -e "AZURE_CLIENT_ID=<ClientID>" -e AZURE_SECRET='"<Secret>"' -e "AZURE_SUBSCRIPTION_ID=<SubscriptionID>" -e "AZURE_TENANT=<TenantID>" -e "VstsAccount=<VstsAccount>" -e VstsToken='"<VstsToken>"' --flush-cache
```