# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
  end

  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 8800, host: 8800
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "forwarded_port", guest: 8081, host: 8081

  config.vm.provision "shell", inline: <<-SHELL
    do-release-upgrade
    sudo apt-get update
    sudo apt-get install -y g++
    sudo apt-get install -y curl
    curl -sL https://deb.nodesource.com/setup_4.x | sudo sh
    sudo apt-get install -y nodejs
    sudo npm i -g npm@latest
    node -v && npm -v
    sudo npm install npme -g --unsafe
  SHELL
end
