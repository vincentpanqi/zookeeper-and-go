Vagrant.configure("2") do |config|
  config.vm.define :go do |go_config|
    go_config.vm.box = "hashicorp/precise64"
    go_config.vm.network "private_network", :ip => "129.168.12.10"
    go_config.vm.provision :shell, :path => "servers/go.sh"
    go_config.vm.synced_folder "examples", "/home/vagrant/examples"
  end

  config.vm.define :zk1 do |zk1_config|
    zk1_config.vm.box = "hashicorp/precise64"
    zk1_config.vm.network "private_network", :ip => "192.168.12.11"
    zk1_config.vm.provision :shell, :path => "servers/zookeeper.sh", :args => "1"
  end
  
  config.vm.define :zk2 do |zk2_config|
    zk2_config.vm.box = "hashicorp/precise64"
    zk2_config.vm.network "private_network", :ip => "192.168.12.12"
    zk2_config.vm.provision :shell, :path => "servers/zookeeper.sh", :args => "2"
  end
  
  config.vm.define :zk3 do |zk3_config|
    zk3_config.vm.box = "hashicorp/precise64"
    zk3_config.vm.network "private_network", :ip => "192.168.12.13"
    zk3_config.vm.provision :shell, :path => "servers/zookeeper.sh", :args => "3"
  end
end
