# INSTALL THE REQUIREMENTS FIRST

### pip install --require-hashes --no-deps  -r https://raw.githubusercontent.com/PaloAltoNetworks/pan-os-ansible/develop/requirements.txt

#### pip install lxml

# pan-ansible

A collection of Ansible Playbook dedicated to Paloaltonetworks equipments

## Example
```
# ansible-playbook palo_version.yml
PLAY [Check PAN equipment OS version] *************************************

TASK [Gathering Facts] ****************************************************
ok: [10.XX.XX.XX]
ok: [10.XX.XX.XX]
ok: [10.XX.XX.XX]

TASK [Set Variables] ******************************************************
ok: [10.XX.XX.XX]
ok: [10.XX.XX.XX]
ok: [10.XX.XX.XX]

TASK [Check OS version on each VM] ****************************************
changed: [10.XX.XX.XX]
changed: [10.XX.XX.XX]
changed: [10.XX.XX.XX]

TASK [set_fact] ***********************************************************
ok: [10.XX.XX.XX]
ok: [10.XX.XX.XX]
ok: [10.XX.XX.XX]

TASK [debug] **************************************************************
ok: [10.XX.XX.XX] => {
    "msg": "VM100 run 8.0.9"
}
ok: [10.XX.XX.XX] => {
    "msg": "VM300 run 8.0.10"
}
ok: [10.XX.XX.XX] => {
    "msg": "Panorama run 8.1.4"
}

PLAY RECAP ****************************************************************
10.XX.XX.XX              : ok=5    changed=1    unreachable=0    failed=0
10.XX.XX.XX               : ok=5    changed=1    unreachable=0    failed=0
10.XX.XX.XX               : ok=5    changed=1    unreachable=0    failed=0
```
# Pan Upgrade

# ansible-playbook -i inventory.txt --ask-vault-pass upgrade-firewall.yml -e "version=10.2.2"
# ansible-playbook -i inventory.txt --ask-vault-pass upgrade-firewall1.yml --limit 38.142.96.19 -e "version=10.2.2"
