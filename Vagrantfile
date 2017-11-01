# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  # Make sure python (for ansible) is installed
  config.vm.provision "shell", inline: 'test -e /usr/bin/python || (apt-get -qqy update && apt-get install -qqy python-minimal)'
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
  config.vm.network :forwarded_port, guest: 8777, host: 8777
  config.vm.network :forwarded_port, guest: 8888, host: 8888
end
