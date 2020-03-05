
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.6.12"
  config.vm.synced_folder "./dependency-check", "/home/ubuntu/dependency-check"
  config.vm.provision "shell", path: "provision.sh"


end
