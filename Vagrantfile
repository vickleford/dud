# -*- mode: ruby -*-
# vi: set ft=ruby :

$script = <<SCRIPT
apt-get install -y apache2
SCRIPT

Vagrant.configure("2") do |config|
  config.vm.box = "precise32"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"
  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.synced_folder ".", "/var/www"
  config.vm.provision :shell, :inline => $script
end
