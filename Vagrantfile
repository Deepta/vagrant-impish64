# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility).
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/impish64"

  config.vm.network "public_network"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "impish64"
    # Display the VirtualBox GUI when booting the machine
    vb.gui = true
    # Customize the amount of resource on the VM:
    vb.cpus = 2
    vb.memory = "4096"
  end

  config.vm.provision "shell", inline: <<-SHELL

    apt update
    apt install -y \
      bind9-utils \
      curl         
   
    # Uncomment for desktop
    # also set  vb.gui = true in the section above to enable desktop gui  
    apt install -y gnome
  SHELL
end