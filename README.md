# ansible-lab

## Host Set-up

* Vagrant

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
```
