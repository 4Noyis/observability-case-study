Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-22.04"
  config.vm.hostname = "monitoring"

  config.vm.network "private_network", ip: "192.168.56.30"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 6144
    vb.cpus = 3
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yaml"
  end
end
