# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
 Vagrant.configure("2") do |config|

    config.vm.define "ans" do |ansctrl|
      ansctrl.vm.box="ubuntu/trusty64"
      ansctrl.vm.hostname="ansctrl"
      ansctrl.vm.network "private_network", ip: "192.168.34.10"
      ansctrl.vm.synced_folder "./data", "/home/vagrant/vagrant_data"
      ansctrl.vm.synced_folder "./../ucis-projects", "/home/vagrant/ucis-projects"
    end

    config.vm.define "wildfly01" do |wildfly01|
      wildfly01.vm.box="ubuntu/trusty64"
      wildfly01.vm.hostname="wildfly01"
      wildfly01.vm.network "private_network", ip: "192.168.34.20"
      wildfly01.vm.network "forwarded_port" ,guest: 80,host:8081
    end

    config.vm.define "db01" do |db01|
      db01.vm.box="ubuntu/trusty64"
      db01.vm.hostname="db01"
      db01.vm.network "private_network",ip:"192.168.34.30"
    end
    config.vm.define "base" do |base|
      base.vm.box="ubuntu/trusty64"
      base.vm.hostname="base"
      base.vm.network "private_network",ip:"192.168.34.40"
      base.vm.network "forwarded_port",guest:80,host:8082
    end
    config.vm.define "mongo01" do |mongo01|
      mongo01.vm.box = "bento/ubuntu-16.04"
      mongo01.vm.network "private_network", ip: "192.168.56.17"
    end

 end
