# ansible-lab

## Ansible Control Machine Prep

* Vagrant & VirtualBox

```
cd ansible
```

Create 'Vagrantfile' with the configuration below.

```
Vagrant.configure("2") do |config|

config.ssh.insert_key = false

  config.vm.define "ansible" do |ansible|
    ansible.vm.box = "ubuntu/trusty64"
    ansible.vm.hostname = "ansible"
    ansible.vm.network "private_network", ip: "192.168.33.10"
  end
end
```
```
vagrant up
vagrant ssh
```

## Installing Ansible

```
sudo apt-get update
sudo apt-get install software-properties-common
sudo apt-add-repository --yes ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```
