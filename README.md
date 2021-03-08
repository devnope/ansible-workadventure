# automated setup from blank debian to a basically usable workadventure instance

## Pretext

This Repository tries to be a help in your quest in deploying your very own WorkAdventure-Instance.
On the other hand, it won't help you in designing your own maps. 

Let's assume, you have the cheapest VPS Instance from Hetzner.

### Problems solved by the Ansible Roles

## Preparation

You can then use the `cloud-init` File as a Kickstarter for your server. 

This prepares you to have a basically working server to which you can logon via ssh with your private key. 
After that you can use git to pull this repository and install Ansible.

Then you should create a Vault-File for Ansible. An example will be provided.

After you filled in the Vault-File, fill in your specific data inside the `deployment.yml`.

## Execution

## Results so far

## ToDos for this Repo:

* provide cloud-init
* provide ansible-vault template
* provide more content for fail2ban
* set zstd to default logrotate Compressor - because ... I can
* improve UFW
* verify/improve Reboot Ѕafety
