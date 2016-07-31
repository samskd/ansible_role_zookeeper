# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "geerlingguy/ubuntu1604"
  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.memory = "2048"

    config.vm.network :forwarded_port, guest: 2181, host: 2181

    config.vm.provision "ansible" do |ansible|
      ansible.tags = "deploy,restart"
      ansible.playbook = "install.yml"
    end
  end
end
