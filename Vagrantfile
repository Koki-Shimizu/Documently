# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|

  config.vm.box = "ubuntu-1110-server-amd64"
  config.vm.box_url = "http://timhuegdon.com/vagrant-boxes/ubuntu-11.10.box"

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.module_path = "modules"
  end

  config.vm.define :clusterer do |c|
    c.vm.network :hostonly, "10.11.12.100"
    c.vm.host_name = 'clusterer'
  end
end
