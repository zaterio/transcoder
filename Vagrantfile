# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.hostname =  "carbon"		
  config.vm.provider :libvirt do |v|
				v.cpus = 1
				v.memory = 512
				v.nested = true
				v.keymap = "es"
				v.volume_cache = "none"
				
  config.vm.provision "ansible" do |an|
			 an.playbook = "ansible/playbooks/transcoder.yml"
			 an.sudo = true
			end	   
end
