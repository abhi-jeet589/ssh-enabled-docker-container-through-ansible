# ssh-enabled-docker-container-through-ansible
Using this repository you can create a SSH enabled docker container through ansible which can then later be used to configure anything within that container through ansible itself.
<h1>Steps to use this repository</h1>
First things first do install ansible on your linux system using the command
`pip install ansible`
After you have installed ansible you can go and check the version of ansible using
`ansible --version`
Next thing to do is to create the config file for ansible that will tell ansible where the inventory file is present.
`touch /etc/ansible/ansible.cfg`
Now enter the following lines in the config file
```
[defaults]
inventory=<location of config.txt in the linux system>
```
<b>Great!!</b> Now follow the steps to run the ansible code
<b>Step 1:</b> Copy all the content to the directory you want
<b>Step 2:</b> Run the ansible command using 
`ansible-playbook setup.yml`
After this enter the values as specified on the prompt in the ansible. You will have a container that can be connected using ansible and can be configured as per your need.
