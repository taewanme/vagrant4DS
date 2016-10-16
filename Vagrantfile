# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
    config.vm.network "private_network", ip: "192.168.33.33"
  # config.vm.synced_folder "../ipython", "/ipython"

  config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
     vb.memory = "5120"
  end

  # config.push.define "atlas" do |push|
  #   push.app = "YOUR_ATLAS_USERNAME/YOUR_APPLICATION_NAME"
  # end

    config.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo apt-get -y install python
      sudo apt-get -y install python-pip
      sudo apt-get -y install build-essential libssl-dev libffi-dev libxml2-dev
      sudo pip install --upgrade pip
      sudo pip install numpy
      sudo pip install pillow
      sudo pip install scipy
      sudo pip install matplotlib
      sudo pip install ipython
      sudo pip install jupyter
      sudo pip install virtualenv
      sudo pip install scikit-learn
      sudo pip install Pandas
      sudo pip install scrapy
      sudo pip install NLTK
      sudo pip install Pattern

      export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-0.11.0rc0-cp27-none-linux_x86_64.whl

      sudo pip install --upgrade $TF_BINARY_URL
      sudo pip install Seaborn
      sudo pip install bokeh
      sudo pip install NetworkX
      sudo cp /vagrant/jupyter.sh ./
      sudo chmod 777 ./jupyter.sh
      sudo mkdir -p /vagrant/ipythons
      sudo chmod 755 /vagrant/ipythons
    SHELL
end
