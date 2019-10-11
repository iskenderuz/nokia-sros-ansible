# Ansible playbooks for SROS orchestration

## Summary
Set of ansible playbook examples to orchestrate SROS.

List of the tasks;
- deploy_vsim
- destroy_vsim
- baseline_router
- yang_collector
- jtox_builder
- prepare_config
- configure_router
- state_intent
- state_scrub

## Usage

### Pre-requisites

1)  Install the following packages and modules on Ansbile host

```
yum -y install epel-release
yum -y install ansible
yum -y install python-pip
pip install pyang
pip install setuptools -U
pip install ncclient
pip install jxmlease
```

2) Ensure you place the following files into the files directory

```
sros-vm.qcow2
license.txt
/YANG
```



### Start, license and configure a vSIM using libvirt on CentOS

```bash
ansible-playbook start.yml
```

### Destroy vSIM using libvirt on CentOS

```bash
ansible-playbook stop.yml
```
