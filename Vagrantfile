Vagrant.configure("2") do |config|

    config.vm.define "rbt01" do |rbt01|
        rbt01.vm.box = "bento/centos-7.4"
        rbt01.vm.hostname = "RBT01"
        second_drive = sprintf('.vagrant/disk_data_%s.vdi', "rbt01")
        rbt01.vm.network "private_network" , ip: "172.28.128.10"
        rbt01.vm.provider "virtualbox" do |v|
            v.cpus = 1
            v.memory = 1024
            v.customize ['createhd', '--filename', second_drive, '--size', 5120]
            v.customize ['storageattach', :id, '--storagectl', 'SATA Controller', '--port', 1, '--device', 0, '--type', 'hdd', '--medium', second_drive]
        end
    end
    
    config.vm.define "rbt02" do |rbt02|
        rbt02.vm.box = "bento/centos-7.4"
        rbt02.vm.hostname = "RBT02"
        second_drive = sprintf('.vagrant/disk_data_%s.vdi', "rbt02")
        rbt02.vm.network "private_network" , ip: "172.28.128.11"
        rbt02.vm.provider "virtualbox" do |v|
            v.cpus = 1
            v.memory = 1024
            v.customize ['createhd', '--filename', second_drive, '--size', 5120]
            v.customize ['storageattach', :id, '--storagectl', 'SATA Controller', '--port', 1, '--device', 0, '--type', 'hdd', '--medium', second_drive]
        end
    end

    config.vm.define "rbt03" do |rbt03|
        rbt03.vm.box = "bento/centos-7.4"
        rbt03.vm.hostname = "RBT03"
        second_drive = sprintf('.vagrant/disk_data_%s.vdi', "rbt03")
        rbt03.vm.network "private_network" , ip: "172.28.128.12"
        rbt03.vm.provider "virtualbox" do |v|
            v.cpus = 1
            v.memory = 1024
            v.customize ['createhd', '--filename', second_drive, '--size', 5120]
            v.customize ['storageattach', :id, '--storagectl', 'SATA Controller', '--port', 1, '--device', 0, '--type', 'hdd', '--medium', second_drive]
        end
    end
    
    config.vm.define "ha1" do |ha1|
        ha1.vm.box = "bento/centos-7.4"
        ha1.vm.hostname = "HA1"
        ha1.vm.network "private_network" , ip: "172.28.128.13"
    end

    config.vm.define "ha2" do |ha2|
        ha2.vm.box = "bento/centos-7.4"
        ha2.vm.hostname = "HA2"
        ha2.vm.network "private_network" , ip: "172.28.128.14"
    end    
end