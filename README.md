# peepcode-chef

Peepcode Chef Recipes. Requires VirtualBox, available at:

https://www.virtualbox.org/wiki/Downloads


## HOWTO by Romain
The following should get you done

    vagrant ssh
    sudo su
    mkdir /etc/chef
    cp /cookbooks/node.json /cookbooks/solo.rb /etc/chef
    apt-get update
    gem update && gem install chef --no-rdoc --no-ri
    # chef-solo -j /etc/chef/node.json
