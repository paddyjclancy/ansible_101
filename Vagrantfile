# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

# Listing Plugins
plugins = ['vagrant-hostsupdater']

# Executing Plugins
plugins.each do |plugin|
	
end

# Vagrant 
Vagrant.configure("2") do |config|
	# Web Virtual Machine
	config.vm.define "web" do |web|
		web.vm.box = "ubuntu/xenial64"
		web.vm.network :private_network, ip: "192.168.0.10"
		web.vm.hostname = "web"
		web.vm.hostsupdater.aliases = ["development.web"] 
	end
	# DB Virtual Machine
	config.vm.define "db" do |db|
		db.vm.box = "ubuntu/xenial64"
		db.vm.network :private_network, ip: "192.168.0.20"
		db.vm.hostname = "db"
		# db.vm.hostsupdater.aliases = ["development.db"] 
	end
	# AWS Virtual Machine
	config.vm.define "aws" do |aws|
		aws.vm.box = "ubuntu/xenial64"
		aws.vm.network :private_network, ip: "192.168.0.30"
		aws.vm.hostname = "aws"
		aws.vm.hostsupdater.aliases = ["development.aws"] 
	end
end
