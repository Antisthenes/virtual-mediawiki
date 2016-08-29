Vagrant.configure("2") do |config|
	config.vm.box = "ubuntu/xenial64"
	
	config.vm.synced_folder ".", "/vagrant"

	config.vm.provision "ansible_local" do |ansible|
		ansible.playbook = "provisioning/playbook.yml"
	end

	config.vm.network :forwarded_port, host: 7777, guest: 80
end

