# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

   config.vm.box = "http://files.vagrantup.com/lucid32.box"
   config.vm.hostname = "RDBMS-box"

   config.vm.network :private_network, ip: "192.168.56.70"
   config.vm.network "forwarded_port", guest: 50000, host: 50000
   config.vm.provision :shell, :path => "provision.sh"

   config.vm.provider :virtualbox do |vb|
     vb.name = "RDBMS-box"
     vb.customize ["modifyvm", :id, "--memory", "1024"]
   end

end

