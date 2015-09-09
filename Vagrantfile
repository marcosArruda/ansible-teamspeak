require 'yaml'

  #config.vm.provision "shell", inline: "sudo mkdir -p /home/vagrant/.docker /root/.docker; chown -R vagrant:vagrant /home/vagrant/.docker; sudo apt-get update"
  #config.vm.provision "file", source: "~/.docker/config.json", destination: "~/.docker/config.json"
  #config.vm.provision "shell", inline: "sudo chmod +rw /home/vagrant/.docker/config.json"
  #config.vm.provision "shell", inline: "sudo cp /home/vagrant/.docker/config.json /root/.docker/config.json"


Vagrant.configure("2") do |config|
  config.vm.hostname = "teamspeak3"
  config.vm.box = "trusty-server-cloudimg-amd64-vagrant-disk1"
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
  config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'"
  config.vm.define "teamspeak3"

  config.vm.provider "virtualbox" do |vb, override|
    vb.name = "teamspeak3"
    vb.memory = 2048
    vb.cpus = 2

    override.vm.network "private_network", ip: "192.168.56.4"

  end

end
