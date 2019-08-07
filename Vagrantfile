$script = <<-SCRIPT

set -ex
cp -R /vagrant/www /home/vagrant && mv /home/vagrant/www /home/vagrant/hello-world
cd /home/vagrant/hello-world
# starting ember
echo starting ember...
npm install
systemctl start ember
# check if the previous command succeeded
if [ $? -eq 0 ]; then
    echo Ember started
else
    echo Ember not started
    exit 1
fi
set +x
SCRIPT

Vagrant.configure("2") do |config|
  config.vm.box = "chavo1/bionic64-ember"
  config.vm.network "forwarded_port", guest:4200, host: 4200
  config.vm.provision "shell", inline: $script
end


