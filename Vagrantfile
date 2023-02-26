Vagrant.configure("2") do |config|

  # Definir o provider e alocar recursos
  config.vm.provider "virtualbox" do |v|
    v.name = "vagrant-docker"
    v.cpus = 1
    v.memory = 1024
    v.gui = false
  end

  # Definir hostname, SO e rede
  config.vm.hostname = "ubuntu"
  config.vm.box = "ubuntu/jammy64"
  config.vm.network "private_network", ip: "192.168.56.11"

  # Compartilhando a pasta que contém o arquivo index.html
  config.vm.synced_folder "./site", "/site"

  # Provisionar VM pelo Shell
  config.vm.provision "shell", path: "provision.sh"

end
