# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # UNCOMMENT CODE BELOW FOR UBUNTU/BIONIC
  # config.vm.box = "ubuntu/bionic64"

  # UNCOMMENT CODE BELOW FOR FEDORA 30
  # config.vm.box = "fedora/30-cloud-base"
  # config.vm.box_version = "30.20190425.0"

  # UNCOMMENT CODE BELOW FOR CENTOS 7
  config.vm.box = "centos/7"

  # UNCOMMENT CODE BELOW FOR DEBIAN JESSIE64
  # config.vm.box = "debian/jessie64"

  # Running the Ansible Code/Playbook
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

  # config.ssh.password = "myBadPassword"
  config.vm.provision "shell", inline: <<-SHELL
    sudo yum update -y
    sudo yum install -y epel-release vim python-pip
    sudo pip install ansible
    # sudo curl https://rclone.org/install.sh | sudo bash
  SHELL
end
