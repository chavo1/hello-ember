# -*- mode: ruby -*-
# vi: set ft=ruby :

$script = <<-SCRIPT

pushd /vagrant/www
systemctl stop ember

[ -d /usr/lib/node_modules/ember-cli ] || npm install -g --no-optional ember-cli
[ -d /usr/lib/node_modules/ember-data ] || npm install -g --no-optional ember-data

npm link ember-cli
npm link ember-data

cp /vagrant/ember.service /etc/systemd/system/ember.service
systemctl daemon-reload
systemctl start ember

SCRIPT

Vagrant.configure("2") do |config|
  config.vm.box = "chavo1/bionic64-ember"
  config.vm.network "forwarded_port", guest:4200, host: 4200
  config.vm.provision "shell", inline: $script
end


