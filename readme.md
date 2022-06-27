
otcamp Week 6 - Ansible

Provisioning servers from central "ansible server/host" created for weight-tracker application.



## Installation

Install ansible with apt

```bash
  sudo apt install ansible
```
    
## Prerequisite
Bare metal or virtual Linux Machine

OR

In case of windows machine you can setup any virtual environment and setup Linux on it.
Or install ubuntu wsl for windows from microsoft store or download from 
https://aka.ms 
ubuntu : Ubuntu_1804.2019.522.0_x64.appx

or whatever Linux flavour you prefered.
 

## Usage/Examples

Create infrastructure and provision servers for weight tracker app


#### Create Infrastructure

##### Staging

	$ Select workspace stage
	$terraform apply  -var-file="environment\stage\stage.tfvars"

##### Production :
	
	$ Select workspace prod
	$terraform apply  -var-file="environment\prod\prod.tfvars"


#### Provisioning Infrastructure for Weight Tracker App

Staging :
	ansible-playbook site.yml -i environments/stage/inventory

Production :
	ansible-playbook site.yml -i environments/prod/inventory



