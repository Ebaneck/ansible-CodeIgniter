# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

# system "vagrant plugin update"
# required_plugins = %w(vagrant-digitalocean)
# required_plugins.each do |plugin|
#   system "NOKOGIRI_USE_SYSTEM_LIBRARIES=1 vagrant plugin install #{plugin}" unless Vagrant.has_plugin? plugin
# end

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.define "webserver" do |web|
    web.vm.hostname = "php"
    web.vm.network "private_network", ip: "33.33.33.37"
    web.vm.provider "virtualbox" do |provider|
      provider.name = "PHP Web Server"
      provider.customize ["modifyvm", :id, "--memory", "1024"]
    end

    web.vm.provision "ansible" do |ansible|
      ansible.playbook = "web-playbook.yml"
      ansible.inventory_path = "hosts"
      ansible.host_key_checking = false
      ansible.sudo = true
    end

  end

end
