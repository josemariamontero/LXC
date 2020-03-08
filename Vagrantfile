
 # -*- mode: ruby -*-
 # vi: set ft=ruby :

 Vagrant.configure("2") do |config|
   config.vm.define :servidorapache do |config|
   config.vm.network :private_network, ip: "192.168.122.101", lxc__bridge_name: 'virbr0'
   config.vm.box="sagiru/buster-amd64"
   config.vm.provider :lxc do |lxc|
     lxc.container_name = :machine
     lxc.container_name = 'servidorapache'
   end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yaml"
  end
end

    config.vm.define :servidormysql do |config|
    config.vm.network :private_network, ip: "192.168.122.102", lxc__bridge_name: 'virbr0'
    config.vm.box="sagiru/buster-amd64"
    config.vm.provider :lxc do |lxc|
      lxc.container_name = :machine
      lxc.container_name = 'servidormysql'
    end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yaml"
  end
  end
end
