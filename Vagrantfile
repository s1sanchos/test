Vagrant.configure("2") do |config|
	
	
	config.vm.disk :disk, size: "10GB", primary: true
	config.vm.box = "debian/jessie64"
	config.vm.synced_folder '.', '/vagrant', disabled: true
	config.vbguest.auto_update = false
	
	
	config.vm.provider "virtualbox" do |vb|
		
		
		vb.memory = "2048"
		vb.cpus = 2
		
	end
	
	config.vm.provision "ansible" do |ansible|
		ansible.playbook = "playbook.yml"
	end
	
	
end

