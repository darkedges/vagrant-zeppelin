# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
    config.hostmanager.enabled = true
    config.hostmanager.manage_host = false
    config.hostmanager.manage_guests = true
    config.hostmanager.ignore_private_ip = false
    config.hostmanager.include_offline = true

    config.vm.define "zeppelin" , autostart: true, primary: true do |zeppelin|
    zeppelin.vm.box = "centos/7"
    zeppelin.vm.hostname = "zeppelin"
    zeppelin.vm.network :private_network, ip: "192.168.50.101"
    zeppelin.hostmanager.aliases = [ "zeppelin.local.darkedges.com" ]

    zeppelin.vm.provider "virtualbox" do |vb|
        vb.customize ["modifyvm", :id, "--memory", "4096"]
        vb.customize ["modifyvm", :id, "--name", "zeppelin"]
        vb.customize ["modifyvm", :id, "--cpus", "2"]
        vb.customize ["modifyvm", :id, "--ioapic", "on"]
        vb.customize ["modifyvm", :id, "--cpuexecutioncap", "75"]
        vb.customize ["modifyvm", :id, "--paravirtprovider", "kvm"]
    end   
    zeppelin.vbguest.auto_update = true
    end
end
