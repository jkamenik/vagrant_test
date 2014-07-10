# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: <<SCRIPT

sudo su
apt-get update
export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true
apt-get install git make golang -y

SCRIPT

  config.vm.define "32bit" do |web|
    web.vm.box = "hashicorp/precise32"
  end

  config.vm.define "64bit" do |db|
    db.vm.box = "hashicorp/precise64"
  end
end
