#  IT-BR Australia Ansible WorkShop 


This is a Sample Code to be used for everyone who wants to understand a little bit more about **`Ansible`**

This code will create an instance on your 
`AWS Account` . So before start to use these playbooks, please configure your environment setting the **`AWS credentials`**.

Use the followed Link to configure the System:

	https://aws.amazon.com/blogs/apn/getting-started-with-ansible-and-dynamic-amazon-ec2-inventory-management/

## Executing the Playbook


To run the Playbook just execute the command line below once you have your AWS account set.

**`ansible-playbook -i hosts main.yml`**

Example of output console:

```
PLAY [local] *********************************************************************************************************************************************************************************************************************************

TASK [Gathering Facts] ***********************************************************************************************************************************************************************************************************************
ok: [localhost]

TASK [infradeploy : Setting Security Groups] *************************************************************************************************************************************************************************************************
changed: [localhost -> localhost]

TASK [infradeploy : Creating AWS Instances] **************************************************************************************************************************************************************************************************
changed: [localhost]

TASK [infradeploy : Wait Instances get Ready] ************************************************************************************************************************************************************************************************
ok: [localhost] => (item={u'ramdisk': None, u'kernel': None, u'root_device_type': u'ebs', u'private_dns_name': u'ip-172-31-15-64.ap-southeast-2.compute.internal', u'block_device_mapping': {u'/dev/sda1': {u'status': u'attached', u'delete_on_termination': True, u'volume_id': u'vol-094c57fcb421968ea'}}, u'key_name': u'itbr-demousr', u'public_ip': u'3.106.170.36', u'image_id': u'ami-0975ce566eec139c3', u'tenancy': u'default', u'private_ip': u'172.31.15.64', u'groups': {u'sg-05dcc97ce830e2a2c': u'ITBR-DEMO'}, u'public_dns_name': u'ec2-3-106-170-36.ap-southeast-2.compute.amazonaws.com', u'state_code': 16, u'id': u'i-08b131e07a6ef301d', u'tags': {}, u'placement': u'ap-southeast-2a', u'ami_launch_index': u'0', u'dns_name': u'ec2-3-106-170-36.ap-southeast-2.compute.amazonaws.com', u'region': u'ap-southeast-2', u'ebs_optimized': False, u'launch_time': u'2019-09-19T04:21:16.000Z', u'instance_type': u't2.micro', u'state': u'running', u'architecture': u'x86_64', u'hypervisor': u'xen', u'virtualization_type': u'hvm', u'root_device_name': u'/dev/sda1'})

TASK [infradeploy : Creating Temp Inventory] *************************************************************************************************************************************************************************************************
changed: [localhost] => (item={u'ramdisk': None, u'kernel': None, u'root_device_type': u'ebs', u'private_dns_name': u'ip-172-31-15-64.ap-southeast-2.compute.internal', u'block_device_mapping': {u'/dev/sda1': {u'status': u'attached', u'delete_on_termination': True, u'volume_id': u'vol-094c57fcb421968ea'}}, u'key_name': u'itbr-demousr', u'public_ip': u'3.106.170.36', u'image_id': u'ami-0975ce566eec139c3', u'tenancy': u'default', u'private_ip': u'172.31.15.64', u'groups': {u'sg-05dcc97ce830e2a2c': u'ITBR-DEMO'}, u'public_dns_name': u'ec2-3-106-170-36.ap-southeast-2.compute.amazonaws.com', u'state_code': 16, u'id': u'i-08b131e07a6ef301d', u'tags': {}, u'placement': u'ap-southeast-2a', u'ami_launch_index': u'0', u'dns_name': u'ec2-3-106-170-36.ap-southeast-2.compute.amazonaws.com', u'region': u'ap-southeast-2', u'ebs_optimized': False, u'launch_time': u'2019-09-19T04:21:16.000Z', u'instance_type': u't2.micro', u'state': u'running', u'architecture': u'x86_64', u'hypervisor': u'xen', u'virtualization_type': u'hvm', u'root_device_name': u'/dev/sda1'})

TASK [infradeploy : Generate Dinamic Inventory] **********************************************************************************************************************************************************************************************
changed: [localhost] => (item={u'ramdisk': None, u'kernel': None, u'root_device_type': u'ebs', u'private_dns_name': u'ip-172-31-15-64.ap-southeast-2.compute.internal', u'block_device_mapping': {u'/dev/sda1': {u'status': u'attached', u'delete_on_termination': True, u'volume_id': u'vol-094c57fcb421968ea'}}, u'key_name': u'itbr-demousr', u'public_ip': u'3.106.170.36', u'image_id': u'ami-0975ce566eec139c3', u'tenancy': u'default', u'private_ip': u'172.31.15.64', u'groups': {u'sg-05dcc97ce830e2a2c': u'ITBR-DEMO'}, u'public_dns_name': u'ec2-3-106-170-36.ap-southeast-2.compute.amazonaws.com', u'state_code': 16, u'id': u'i-08b131e07a6ef301d', u'tags': {}, u'placement': u'ap-southeast-2a', u'ami_launch_index': u'0', u'dns_name': u'ec2-3-106-170-36.ap-southeast-2.compute.amazonaws.com', u'region': u'ap-southeast-2', u'ebs_optimized': False, u'launch_time': u'2019-09-19T04:21:16.000Z', u'instance_type': u't2.micro', u'state': u'running', u'architecture': u'x86_64', u'hypervisor': u'xen', u'virtualization_type': u'hvm', u'root_device_name': u'/dev/sda1'})

TASK [infradeploy : Setting Instance TAG] ****************************************************************************************************************************************************************************************************
changed: [localhost] => (item={u'ramdisk': None, u'kernel': None, u'root_device_type': u'ebs', u'private_dns_name': u'ip-172-31-15-64.ap-southeast-2.compute.internal', u'block_device_mapping': {u'/dev/sda1': {u'status': u'attached', u'delete_on_termination': True, u'volume_id': u'vol-094c57fcb421968ea'}}, u'key_name': u'itbr-demousr', u'public_ip': u'3.106.170.36', u'image_id': u'ami-0975ce566eec139c3', u'tenancy': u'default', u'private_ip': u'172.31.15.64', u'groups': {u'sg-05dcc97ce830e2a2c': u'ITBR-DEMO'}, u'public_dns_name': u'ec2-3-106-170-36.ap-southeast-2.compute.amazonaws.com', u'state_code': 16, u'id': u'i-08b131e07a6ef301d', u'tags': {}, u'placement': u'ap-southeast-2a', u'ami_launch_index': u'0', u'dns_name': u'ec2-3-106-170-36.ap-southeast-2.compute.amazonaws.com', u'region': u'ap-southeast-2', u'ebs_optimized': False, u'launch_time': u'2019-09-19T04:21:16.000Z', u'instance_type': u't2.micro', u'state': u'running', u'architecture': u'x86_64', u'hypervisor': u'xen', u'virtualization_type': u'hvm', u'root_device_name': u'/dev/sda1'})

PLAY RECAP ***********************************************************************************************************************************************************************************************************************************
localhost                  : ok=7    changed=5    unreachable=0    failed=0
```


**AWS DashBoard**

![AWS-DASHBOARD](https://github.com/borgessc/ansible_it.br/blob/master/images/AWS-EC2-Dashboard.png)

# Destroying the Test Environment


**# Terminate every running instance in a region. Use with EXTREME caution.**

# **`Don't Use this Playbook in Production Environment`**

Once you done with your tests and to avoid to keep consuming AWS resources you can destroy the Instances that you Created, for this just execute:

**`ansible-playbook -i hosts destroy_instances.yml`**


Example of output console

```
PLAY [Terminate tagged instances] **************************************************************************************************************

TASK [Gathering Facts] **************************************************************************************************************
ok: [localhost]

TASK [Destroying the Current Running Instances] **************************************************************************************************************
ok: [localhost]

TASK [Delete group by name ITBR-DEMO] **************************************************************************************************************
ok: [localhost]

TASK [Delete Dinamic Public IPs] **************************************************************************************************************
changed: [localhost]

PLAY RECAP **************************************************************************************************************
localhost                  : ok=4    changed=1    unreachable=0    failed=0
```  

# Errors and Troubleshooting



**If you face these issues please follow the resolution below.**

_Error #1_

```
52.63.7.124 | UNREACHABLE! => {
    "changed": false,
    "msg": "Failed to connect to the host via ssh: Connection closed by 52.63.7.124 port 22",
    "unreachable": true
}
```
**Solution for #1**

Create a file `ansible.cfg` on project root folder with this content. 
```
[defaults]
private_key_file=/path/of/your/key-file.pem
```


_Error #2_

```
52.63.7.124 | FAILED! => {
    "changed": false,
    "module_stderr": "Shared connection to 52.63.7.124 closed.\r\n",
    "module_stdout": "/bin/sh: 1: /usr/bin/python: not found\r\n",
    "msg": "MODULE FAILURE\nSee stdout/stderr for the exact error",
    "rc": 127
}
```
**Solution for #2**

Install python on target Machine, for example 

if you have python3 installed just create a softlink for that binary.

` ln -s /usr/bin/python3 /usr/bin/python `

**or**

` apt install python `

