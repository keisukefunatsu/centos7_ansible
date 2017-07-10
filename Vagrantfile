# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  # vagrant-cachier
  if Vagrant.has_plugin?('vagrant-cachier')
    config.cache.scope = :box
  end


  config.vm.box = "wate/centos-7"
  config.vm.define 'centos7' do |centos7|
    centos7.vm.network "private_network", ip: "192.168.100.100"
    centos7.vm.provider 'virtualbox' do |v|
      v.name = 'centos7'
      v.customize ["modifyvm", :id, "--ostype", "Redhat_64"]
    end
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end
end
