# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "flynn-precise64"
  config.vm.box_url = "https://s3.amazonaws.com/flynn/flynn-virtualbox-ubuntu_12.04.3-amd64.box"
  config.vm.box_download_checksum = "d222d515e83e0d8a547c55f9e5cbaec703fd414f0d761193d9fee1c6066504cf"
  config.vm.box_download_checksum_type = "sha256"

  config.vm.provision :shell, inline: <<-SCRIPT
    sudo -u vagrant sh -c "echo 'export GOPATH=/home/vagrant/.go' >> /home/vagrant/.bashrc"
    sudo -u vagrant sh -c "echo 'PATH=/home/vagrant/.go/bin:/vagrant/scripts/vagrant:$PATH' >> /home/vagrant/.bashrc"
    sudo -u vagrant sh -c "echo 'cd /vagrant' >> /home/vagrant/.bashrc"
  SCRIPT
end