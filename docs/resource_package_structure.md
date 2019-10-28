# Resource Package Structure for Ansible Lifecycle Driver

The Brent resource package contains Ansible inventory configuration and scripts used by the Ansible Lifecycle Driver. The structure of the directory within the package is defined by the driver. Under this top level directory the driver expects the following directory structure:

```
config
  inventory
  inventory.k8s
scripts
  *.yaml
```

The config directory contains [Ansible inventory](https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html) related configuration files. [Ansible Inventory](./ansible_inventory.md) describes how to construct these files.

The scripts directory contains your Ansible scripts. The naming must reflect the naming of the lifcycle and operation scripts defined in your LM resource.yaml file; the naming is case-sensitive but the extension can be either 'yml' or 'yaml'. Ancillary files can be added under the scripts directory and these will be included in the payload to the Ansible Lifecycle Driver.