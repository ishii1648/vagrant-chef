# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  #box名
  config.vm.box = "centos67"
  #host名
  config.vm.hostname = "chef"
  #ipアドレス
  config.vm.network "public_network", ip: "192.168.1.10"
  #デフォルトの同期を停止
  config.vm.synced_folder ".", "/vagrant", disabled: true
  #chefの実行環境を作成
  config.vm.provision "shell", path: 'provision/scripts/install_chef.sh'
  #chefを実行
  #config.vm.provision "shell", path: 'provision/scripts/chef_execute.sh'

  config.vm.provider "virtualbox" do |vb|
	  vb.memory = 2048
    vb.name   = "chef"
  end
end
