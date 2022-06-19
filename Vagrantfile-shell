
Vagrant.configure("2") do |config|


config.vm.disk :disk, size: "10GB", primary: true
config.vm.box = "debian/jessie64"

config.vbguest.auto_update = false
  
  
   config.vm.provider "virtualbox" do |vb|
  
    vb.memory = "2048"
	vb.cpus = 2
    
end

config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
	sudo apt-get upgrade 
    sudo apt-get dist-upgrade
    sudo apt-get install -y apache2
	sudo apt-get install -y vim
	sudo apt-get install -y wget
	sudo apt-get install -y htop
	sudo apt-get install -y tmux
	sudo apt-get install -y php5
	sudo apt-get install -y nginx
   SHELL
end



