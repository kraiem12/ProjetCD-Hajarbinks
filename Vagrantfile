Vagrant.configure("2") do |config|
  
  config.vm.box = "geerlingguy/centos7"


    config.vm.provider "virtualbox" do |vb|

    	vb.memory = 6301
    	vb.cpus = 1
    end

    config.vm.define "mongodb" do |mongodb|
    	mongodb.vm.hostname = "mongodb.binks"
    	mongodb.vm.network "public_network", bridge: "p8p1",
    	#ip: '192.168.100.114'
    	use_dhcp_assigned_default_route: true
    end
    
    config.vm.define "kubernetes" do |kubernetes|
    		kubernetes.vm.hostname = "kubernetes.binks"
    		kubernetes.vm.network "public_network", bridge: "p8p1",
    	#	ip: "192.168.100.113"
    	use_dhcp_assigned_default_route: true
    end
end
