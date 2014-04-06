Vagrant.configure("2") do |c|

  c.vm.define "master" do |master|
    master.vm.box = "opscode-ubuntu-12.04"
	master.vm.box_url = "https://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_ubuntu-12.04_chef-provisionerless.box"
	master.vm.hostname = "master.vagrantup.com"
	master.vm.network(:private_network, {:ip=>"192.168.33.27"})
	master.vm.provider :virtualbox do |p|
	  p.customize ["modifyvm", :id, "--memory", "256"]
	end
  end

  c.vm.define "target01" do |one|
    one.vm.box = "opscode-ubuntu-12.04"
	one.vm.box_url = "https://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_ubuntu-12.04_chef-provisionerless.box"
	one.vm.hostname = "target01.vagrantup.com"
	one.vm.synced_folder ".", "/vagrant", disabled: true
	one.vm.network(:private_network, {:ip=>"192.168.33.21"})
	one.vm.provider :virtualbox do |p|
	  p.customize ["modifyvm", :id, "--memory", "256"]
	end
  end

  c.vm.define "target02" do |two|
    two.vm.box = "opscode-ubuntu-12.04"
	two.vm.box_url = "https://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_ubuntu-12.04_chef-provisionerless.box"
	two.vm.hostname = "target02.vagrantup.com"
	two.vm.synced_folder ".", "/vagrant", disabled: true
	two.vm.network(:private_network, {:ip=>"192.168.33.22"})
	two.vm.provider :virtualbox do |p|
	  p.customize ["modifyvm", :id, "--memory", "256"]
	end
  end

end
