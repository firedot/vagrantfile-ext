# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "firedot/xenial"
  config.vm.hostname = "bananas3"
  config.vm.network "private_network", ip: "192.168.56.56"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.provision "shell", path: "./scripts/web.sh" 
end
