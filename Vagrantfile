# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-18.04"
  config.vm.define "prometheus" do |prometheus|
    prometheus.vm.network :private_network, ip: "192.168.4.15"
    prometheus.vm.hostname = "prometheus"

    prometheus.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
      ansible.compatibility_mode = "2.0"
    end
  end
end