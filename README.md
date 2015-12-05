# Ansible Playbooks for FreeBSD

Requirements: 

* A FreeBSD 9 or 10 host
* Ansible 1.9 or 2.0

## Poudriere

A quick role to deploy Poudriere, your favorite FreeBSD packet builder.

### Vars tweaking

To tweak these vars, edit `playbooks/vars/poudriere.yml`

* `poudriere_basefs`: where your jails and ports go.
* `poudriere_data`: place to deploy the built packages.
* `poudriere_distfile_cache`: ports distfile cache.
* `poudriere_ftp`: where to fetch the ports.
* `poudriere_zpool`: the zpool to use. Leave empty if you don't use ZFS.
* `freebsd_release`: FreeBSD release to build against.

```
ansible-playbook inventories/main playbooks/poudriere.yml
```
