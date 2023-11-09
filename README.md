# cyberpanel-install-ansible
Ansible Script to automate installation of Cyberpanel Control Panel in Almalinux and Ubuntu

Note: This script is tested on vultr 22.04 vps

## Run it using
```
time ansible-playbook main.yaml
```

## Run it as root using
```
time ansible-playbook main.yaml -u root
```

## Reset Admin Password using:
`adminPass newpassword`
where 'newpassword' is your new strong password (Password should not contain special charecters)


# Migration
## cPanel to cyberpanel
```
mkdir /home/backup
```
upload backup file to /home/backup
then run
```
/usr/local/CyberCP/bin/python /usr/local/CyberCP/plogical/cPanelImporter.py --path /home/backup
```
