Vagrant.configure("2") do |config|
  config.vm.define "master1" do |master1|
    master1.vm.box = "ubuntu/xenial64"
    master1.vm.box_check_update = false
    master1.vm.network "private_network", ip: "192.168.33.10"
    master1.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory = "4096"
    end
    master1.vm.provision "file", source: "~/.ssh/id_rsa.pub", destination: "~/.ssh/me.pub"

    master1.vm.provision "shell", inline: <<-SHELL
      # apt-get update
      cat /home/vagrant/.ssh/me.pub >> /home/vagrant/.ssh/authorized_keys
      # apt-get install docker.io -y 
      # usermod -aG docker vagrant
    SHELL
  end

  config.vm.define "master2" do |master2|
    master2.vm.box = "ubuntu/xenial64"
    master2.vm.box_check_update = false
    master2.vm.network "private_network", ip: "192.168.33.11"
    master2.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory = "1024"
    end
    master2.vm.provision "file", source: "~/.ssh/id_rsa.pub", destination: "~/.ssh/me.pub"

    master2.vm.provision "shell", inline: <<-SHELL
      # apt-get update
      cat /home/vagrant/.ssh/me.pub >> /home/vagrant/.ssh/authorized_keys
      # apt-get install docker.io -y 
      # usermod -aG docker vagrant
    SHELL
  end

  config.vm.define "master3" do |master3|
    master3.vm.box = "ubuntu/xenial64"
    master3.vm.box_check_update = false
    master3.vm.network "private_network", ip: "192.168.33.12"
    master3.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory = "1024"
    end
    master3.vm.provision "file", source: "~/.ssh/id_rsa.pub", destination: "~/.ssh/me.pub"

    master3.vm.provision "shell", inline: <<-SHELL
      # apt-get update
      cat /home/vagrant/.ssh/me.pub >> /home/vagrant/.ssh/authorized_keys
      # apt-get install docker.io -y 
      # usermod -aG docker vagrant
    SHELL
  end

  config.vm.define "master4" do |master4|
    master4.vm.box = "ubuntu/xenial64"
    master4.vm.box_check_update = false
    master4.vm.network "private_network", ip: "192.168.33.13"
    master4.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory = "1024"
    end
    master4.vm.provision "file", source: "~/.ssh/id_rsa.pub", destination: "~/.ssh/me.pub"

    master4.vm.provision "shell", inline: <<-SHELL
      # apt-get update
      cat /home/vagrant/.ssh/me.pub >> /home/vagrant/.ssh/authorized_keys
      # apt-get install docker.io -y 
      # usermod -aG docker vagrant
    SHELL
  end
end

