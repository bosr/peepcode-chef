# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "squeeze64-ruby193"
  config.vm.box_url = "http://packages.diluvia.net/squeeze64-ruby193.box"
  config.vm.network :private_network, ip: "33.33.33.10"
  # config.vm.network :bridged
  # config.vm.forward_port 80, 4567
  config.vm.synced_folder ".", "/cookbooks"

  config.vm.provision :shell, 
    :inline => "mkdir /etc/chef; cp /cookbooks/node.json /cookbooks/solo.rb /etc/chef; apt-get update; gem update && gem install chef --no-rdoc --no-ri; chef-solo -j /etc/chef/node.json"
end
