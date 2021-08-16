# automated setup from blank debian to a basically usable workadventure instance

## Pretext

This Repository tries to be a help in your quest in deploying your very own WorkAdventure-Instance.
On the other hand, it won't help you in designing your own maps. 

Let's assume, you have the cheapest VPS Instance from Hetzner.

### Problems solved by the Ansible Roles

## Preparation

You can then use the `user-data` functionality of Cloud-Init as a Kickstarter for your server. 

This prepares you to have a basically working server to which you can logon via ssh with your private key. 
After that you can use git to pull this repository and install Ansible.

Then you should create a Vault-File for Ansible and name it "vars.vault.yml". An example is provided in "vault-template.yml".

After you filled in the Vault-File, fill in your specific data inside the `deployment.yml`.
```
workadventure_domain: "workadventure.<domain>"
workadventure_start_room: "/_/global/raw.githubusercontent.com/raumzeitlabor/rc3-map-lounge/main/main.json"
jitsi_url: "<jitsii-server>"
```
## Execution

### Execute Ansible:
```
ansible-playbook deployment.yml -e @vars.vault.yml --ask-vault-pass
```

**Reboot is necessary**

### Setup DNS:
This depends on your Domain Provider but the Following should help you:
```
workadventure 600 IN A <ip>
api.workadventure 600 IN A <ip>
back.workadventure 600 IN A <ip>
maps.workadventure 600 IN A <ip>
play.workadventure 600 IN A <ip>
pusher.workadventure 600 IN A <ip>
uploader.workadventure 600 IN A <ip>
coturn.workadventure 600 IN A <ip>
```

### Start Workadventure
```
cd /opt/workadventure/contrib/docker
docker-compose up -d
```

access `https://play.workadventure.<domain>` in your Browser



## ToDos for this Repo:

* provide more content for fail2ban
* improve UFW config
