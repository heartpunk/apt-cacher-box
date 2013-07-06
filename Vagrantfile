#!/usr/bin/env ruby
# coding: utf-8

Vagrant.configure('2') do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--memory", "128"]
  end
  config.vm.network :public_network
  config.vm.network :forwarded_port, guest: 22, host: 4444

  config.vm.provision :shell do |shell|
    shell.inline = "apt-get update && apt-get install -y apt-cacher-ng"
    shell.inline = "ifconfig | grep 'inet addr' | perl -pe 's/inet addr:((\d{1,3}\.){3}\d{1,3}).*/$1/'"
  end
end
