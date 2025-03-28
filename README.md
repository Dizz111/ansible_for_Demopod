# Ansible and Vmware 8.0

Repository for demoPod scripting for Test Drives

Based on pyvmomi=8.0.3.0.1,  ansible [core 2.18.4], python version = 3.12.3

Install virtualenv , Ansible and pyVmomi. ssh keys are assumed set up on control host /laptop

Python should already be installed on control host or laptop - this is tested from an ubuntu 24.04 node
it is best to run this from a **virtual environment** - this can be set up like this:

# virtualenv
sudo apt install python3-venv

python3 -m venv xxx

source xxx/bin/activate

*where xxx = the name you want it to be 

source xxx/bin/activate - puts you in that Virtual env xxx 

deactivate - exits the virtual env

# pip
If you need to install ansible you can use pip if you need pip install it by running this command

sudo apt update

sudo apt install python3-pip

pip3 --version

# ansible
Once pip is installed, we can use it to install Ansible with the following command.

sudo pip install ansible or sudo apt install ansible

# PyVmomi
We also need to install pyVmomi which is the Python SDK for the VMware vSphere API that allows you to manage ESX, ESXi, and vCenter.

pip3 install PyVmomi

pip show pyvmomi

# community.vmware
you also need to make sure community.vmware collection is installed 

ansible-galaxy collection install community.vmware - if not installed

ansible-galaxy collection list - to verify it is installed

# Vsphere 
Not required but It is best to create ansible service user with dedicated role. You can also use administrator@vsphere.local or whatever 

account, but It’s a good practice to create separate accounts for different systems.

