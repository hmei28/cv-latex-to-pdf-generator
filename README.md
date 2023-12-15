# About cv-latex-to-pdf-generator
Ansible role to generate cv pdf from latex and push to google drive

## Requirements
- Ansible >= v2.10.0
- Docker >= 20
- Rclone access Token to google drive 

## Getting Started

Edit /inventory/group_vars/all/common.yaml to spécify all your information 
Edit /inventory/group_vars/all/secret.yaml to add access api to google drive : 
```bash 
rclone_gdrive_token: 
  access_token: "XXXXXX"
  token_type: "Bearer"
  refresh_token : "XXXXXX"
  expiry : "20XX-XX-XXTXX:XX:XX"

mobile: "+336 XX XX XX XX"
address: ""

```
Vault file secret
```bash 
ansible-vault encrypt ./inventory/group_vars/all/secret.yaml
```

Run Plaubook

```bash
ansible-playbook playbook.yaml  --ask-vault-pass
```
