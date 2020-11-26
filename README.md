# Ansible rolne: nfvbench-ansible-role

This repo hosts the `nfvbench-ansible-role` Ansible role.

This role aims to deploy [NFVbench](https://github.com/opnfv/nfvbench) tool inside an SR-IOV VM on a Openstack platform.
The role includes tasks using the `openstack.cloud` Ansible Collection.

## Installation and Usage

### Installing dependencies

For using the NFVbench Ansible role firstly you need to install `ansible` and `openstacksdk` Python modules on your Ansible controller.
For example with pip:

```bash
pip install ansible openstacksdk
```

OpenStackSDK has to be available to Ansible and to the Python interpreter on the host, where Ansible executes the module (target host).
Please note, that under some circumstances Ansible might invoke a non-standard Python interpreter on the target host.
Using Python version 3 is required for OpenstackSDK.

---

#### NOTE

OpenstackSDK is better to be the last stable version. It should NOT be installed on Openstack nodes,
but rather on operators host (aka "Ansible controller"). OpenstackSDK from last version supports
operations on all Openstack cloud versions. Therefore OpenstackSDK module version doesn't have to match
Openstack cloud version usually.

---

### Installing the Openstack Cloud Collection from Ansible Galaxy

Before using this ansible role you need to install the Openstack Cloud collection with the `ansible-galaxy` CLI:

`ansible-galaxy collection install -r requirements.yml`

### Installing the NFVbench ansible role from Ansible Galaxy

Before using this ansible role you need to install the Openstack Cloud collection with the `ansible-galaxy` CLI:

`ansible-galaxy install nfvbench-ansible-role`


### Playbooks

To use this role, please reference the full name of Ansible role, collection name, and module name that you want to use:

```yaml
---
- hosts: localhost
  roles:
    - role: nfvbench-ansible-role

```



## Testing and Development

TBD

### Testing with `ansible-test`

We use `ansible-test` for sanity:

```bash
tox -e linters
```

## More Information

TBD
