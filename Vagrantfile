Vagrant.configure("2") do |config|

	config.vm.define :kali do |kali_config|
		kali_config.vm.box = "offensive-security/kali-linux"
		#не обновлять
		kali_config.vm.box_check_update = false
		#задать hostname машине
		kali_config.vm.hostname = "otus.kali"
		kali_config.vm.provider "virtualbox" do |vbk|
				#задать имя машине
				vbk.name = "otus.kali"
     			vbk.gui = false
     			vbk.memory = "2048"
				vbk.cpus = 2
		end
		#настройка двух интерфейсов
		kali_config.vm.network "private_network", ip: "10.30.30.1", netmask: "255.255.255.0"
		kali_config.vm.network "private_network", ip: "10.20.20.1", netmask: "255.255.255.0"
  	end

	config.vm.define :centos do |centos_config|
		centos_config.vm.box = "centos/7"
        centos_config.vm.box_check_update = false
        centos_config.vm.hostname = "otus.centos"
		centos_config.vm.provider "virtualbox" do |vbc|
				vbc.name = "otus.centos"
                vbc.gui = false
                vbc.memory = "2048"
                vbc.cpus = 2
        end
		centos_config.vm.network "private_network", ip: "10.30.30.2" , netmask: "255.255.255.0"
		centos_config.vm.network "private_network", ip: "10.20.20.2" , netmask: "255.255.255.0"

	end
end

