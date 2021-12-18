# ansible-vmware-linux-create_vm
Automating Red Hat VM deploy on VMware with Ansible

## PLaybooks:

1.newVm.yml - Create a new RHEL 7 VM from scratch by using an image file (ISO) of the OS. You must fill both **config_new.yml** and **credentials.yml** configuration files stored in config_files folder.
2.TransformToTemplate.yml - Convert the VM created previously in a VMWare template. It will be necessary case your object is create new machines using it as a template (clone). You must fill both **config_new.yml** and **credentials.yml** configuration files stored in config_files folder.
3.cloneFromTemplate.yml - Create a new virtual machine from a VMWare template created previously. You must fill both **config_clone.yml** and **credentials.yml** configuration files stored in config_files folder.
4.1.updateVMTools.yml - It will update the VMTools to the last version supported by the Operation System. Please, always check both **config_clone.yml** configuratio file in order to avoid mistakes by running this playbook.
4.2.yumUpdate.yml - It will update all packages installed in the VM since your VM is subscribed on RHSM. Please, always check both **config_clone.yml** configuration file in order to avoid mistakes by running this playbook.

## Run:

```$ ansible-playbook <PLAYBOOK.yml>```
