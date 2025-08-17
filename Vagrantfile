# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

    # box for Ubuntu 14.04 (Trusty Tahr)
    # config.vm.box = "ubuntu/trusty64"

    # box for Ubuntu 22.04 (Jammy Jellyfish)
    config.vm.box = "ubuntu/jammy64"

    # Run the script on the VM after copying it
    config.vm.provision "shell", inline: <<-SHELL
      touch /home/vagrant/install_docker.sh
      chmod 777 /home/vagrant/install_docker.sh


      echo "pattern" > /home/vagrant/install_docker.sh

      echo "pattern2" > /home/vagrant/install_docker.sh

      sed -i 's/pattern2/replacement/' /home/vagrant/install_docker.sh



      
      
      
      
      



      sed -i '1i sudo apt-get update' /home/vagrant/install_docker.sh
      sed -i '2i sudo apt-get install ca-certificates curl' /home/vagrant/install_docker.sh
      sed -i '3i sudo install -m 0755 -d /etc/apt/keyrings' /home/vagrant/install_docker.sh
      sed -i '4i sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc' /home/vagrant/install_docker.sh
      sed -i '5i sudo chmod a+r /etc/apt/keyrings/docker.asc' /home/vagrant/install_docker.sh

      sed -i '6i       echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null' /home/vagrant/install_docker.sh



      sed -i '7i sudo apt-get update' /home/vagrant/install_docker.sh

      sed -i '8i sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin' /home/vagrant/install_docker.sh



      sed -i '9d' /home/vagrant/install_docker.sh


      #/home/vagrant/install_docker.sh





      touch /home/vagrant/Dockerfile
      chmod 777 /home/vagrant/Dockerfile

      echo "pattern" > /home/vagrant/Dockerfile

      sed -i '1i FROM php:7-fpm' /home/vagrant/Dockerfile
      sed -i '2i ADD this_is_an_example.sh /' /home/vagrant/Dockerfile
      sed -i '3i RUN bash -c "/this_is_an_example.sh"' /home/vagrant/Dockerfile

      sed -i '4d' /home/vagrant/Dockerfile







      touch /home/vagrant/this_is_an_example.sh
      chmod 777 /home/vagrant/this_is_an_example.sh

      echo "pattern" > /home/vagrant/this_is_an_example.sh

      sed -i '1i echo "This is an example"' /home/vagrant/this_is_an_example.sh

      sed -i '2d' /home/vagrant/this_is_an_example.sh




    SHELL
  
    config.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
end
