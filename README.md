# README - ansible-playbooks

Clone this repository, create a new folder for your inventory and include `group_vars`
and `host_vars`.

```bash
mkdir -p inventories/production/group_vars \
		 inventories/production/host_vars
```

Start by running the `00-setup-all.yaml` playbook which will run the following
supporting playbooks:

* `10-setup-ansible-local-host.yaml`
* `10-setup-network-hosts.yaml`

### `10-setup-ansible-local-host.yaml`

Performs common setup commands on the local ansible host.

* Generate local ssh key for use by ansible.
* Clone supporting publically available playbooks into roles.  Currently those include:
  * [telegraf](https://github.com/rossmcdonald/telegraf.git)


### `10-setup-network-hosts.yaml`
