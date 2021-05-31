[![Build Status](https://drone.kiwi-labs.net/api/badges/Diesel-Net/pi-hole/status.svg)](https://drone.kiwi-labs.net/Diesel-Net/pi-hole)

# pi-hole
Sets up [Pi-Hole](https://pi-hole.net/) on the internal network.

## Installing External Dependencies
Ansible `2.10.3` was used at the time of this writing.
```bash
ansible-galaxy install -r .ansible/roles/requirements.yaml -p .ansible/roles --force
```

## Deploy
```bash
ansible-playbook .ansible/deploy.yaml -i .ansible/inventories/development/hosts --vault-id ~/.tokens/vault.txt
```
