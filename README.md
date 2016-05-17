# ovirt_host_add Ansible role

This role will install ovirt 3.6 hosted engine.
When this role is run on a fresh infrastructure the hosted engine is installed.
Once the play has been run you will need to add your first data domain for your VMs.When the first VM data domain has been added the hosted engine's data domain will appear and the hosted VM will display as being up.

To add more hosts to a datacenter just run this role on another host.


##Requirements
Centos 7
Ansible 1.4 and a above

##Role variables
* ovirt_host_add_host_hostID: 
each host needs a unique ID.

* ovirt_host_add_host_fqdn: 
FQDN for the host being installed.

* ovirt_host_add_host_master_password: 
Password for the first host in the datacenter.

* ovirt_host_add_host_master_fqdn:
FQDN of the first host in the datacenter.

* ovirt_host_add_engine_appHostName:
Name of the host as show in the UI. 

* ovirt_host_add_engine_cpu_model:
Name of the minimal cpu model allowed.

* ovirt_host_add_engine_user:
Username for the hosted engine.

* ovirt_host_add_engine_password:
Password for the hosted engine.

* ovirt_host_add_engine_domain:
Engine domain name.

* ovirt_host_add_engine_fqdn:
FQDN for the hosted engine.

* ovirt_host_add_engine_ip:
IP address for the hosted engine.

* ovirt_host_add_engine_gateway: 
Gateway address fpr hosted engine.

* ovirt_host_add_engine_storageDomainConnection: 
IP or url for hosted engine storage server(NFS)

* ovirt_host_add_engine_ovirt_engine_appliance: 
The appliance used for the hosted engine.

* ovirt_host_add_engine_vmMemSizeMB:
Size of ram ro allocate to hosted engine(minimum requirement 16gig).

* ovirt_host_add_engine_vmVCpus:
Total CPUs to use for hosted engine.

## Example Playbook
```yaml
- hosts: ovirt_host
  roles:
    - ovirt_host_add
```

See defaults for values.