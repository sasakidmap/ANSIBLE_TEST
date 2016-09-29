# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provider :virtualbox do |vb|
    vb.name = "ansible_test"
    vb.customize ["modifyvm", :id, "--memory", 1024]
    vb.customize ["modifyvm", :id, "--natdnsproxy1", "off"]
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "off"]
  end

  config.vm.box_url = "https://github.com/2creatives/vagrant-centos/releases/download/v6.5.3/centos65-x86_64-20140116.box"
  config.vm.box = "ANSIBLE_TEST"
  config.vm.hostname = "ANSIBLETEST"
  config.vm.network :private_network, ip: "192.168.56.13"

  if Vagrant.has_plugin?("vagrant-cachier")
    config.cache.scope = :box
  end

end
