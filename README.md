# ovirt_host_add Ansible role

This role will install ovirt 3.6 hosted engine.
When this role is run on a fresh infrastructure the hosted engine is installed.
Once the play has been run you will need to add your first data domain for your VMs.When the first VM data domain has been added the hosted engine's data domain will appear and the hosted VM will display as being up.

To add more hosts to a datacenter just run this role on another host.


##Requirements
Centos 7
Ansible 1.4 and a above

##Role variables
* ovirt_host_add.host_hostID: 
each host needs a unique ID.

* host_fqdn: 
FQDN for the host being installed.

* host_master_password: 
Password for the first host in the datacenter.

* host_master_fqdn:
FQDN of the first host in the datacenter.

* engine_appHostName:
Name of the host as show in the UI. 

* engine_cpu_model:
Name of the minimal cpu model allowed.

* engine_user:
Username for the hosted engine.

* engine_password:
Password for the hosted engine.

* engine_domain:
Engine domain name.

* engine_fqdn:
FQDN for the hosted engine.

* engine_ip:
IP address for the hosted engine.

* engine_gateway: 
Gateway address fpr hosted engine.

* engine_storageDomainConnection: 
IP or url for hosted engine storage server(NFS)

* engine_ovirt_engine_appliance: 
The appliance used for the hosted engine.

* engine_vmMemSizeMB:
Size of ram ro allocate to hosted engine(minimum requirement 16gig).

* engine_vmVCpus:
Total CPUs to use for hosted engine.

## Example Playbook
```yaml
- hosts: ovirt_host
  roles:
    - ovirt_host_add
```

See defaults for values.