# -*- mode: ruby -*- 
# vi: set ft=ruby : vsa
Vagrant.configure(2) do |config| 
 config.vm.box = "centos/7" 
# config.vm.box_version = "2004.01" 
 config.vm.provider "virtualbox" do |v| 
 v.memory = 1024 
 v.cpus = 2 
 end 
 config.vm.define "monit" do |monit| 
 monit.vm.network "private_network", ip: "192.168.56.10",  virtualbox__intnet: "net1" 
 monit.vm.network "forwarded_port", guest: 9090, host: 9090
 monit.vm.network "forwarded_port", guest: 9100, host: 9100
 monit.vm.network "forwarded_port", guest: 3000, host: 3000
 monit.vm.network "forwarded_port", guest: 9093, host: 9093
 monit.vm.hostname = "monit" 
 end 
 config.vm.provision "ansible" do |ansible|
 ansible.playbook = "install-prometheus.yml"
 ansible.become = "true"
 end
end 
