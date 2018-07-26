Vagrant.configure("2") do |config|

    ############## RABBITMQ ##############
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
    
    
   ############## HA-PROXY ############## 
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
    
    ############## ELK ##############
    
    # config.vm.define "lgs01" do |lgs01|
    #     lgs01.vm.box = "bento/centos-7.4"
    #     lgs01.vm.hostname = "lgs01"
    #     second_drive = sprintf('.vagrant/disk_data_%s.vdi', "lgs01")
    #     lgs01.vm.network "private_network" , ip: "172.28.128.20"
    #     lgs01.vm.provider "virtualbox" do |v|
    #         v.cpus = 3
    #         v.memory = 2048
    #     end
    # end
        
    # config.vm.define "els01" do |els01|
    #     els01.vm.box = "bento/centos-7.4"
    #     els01.vm.hostname = "els01"
    #     second_drive = sprintf('.vagrant/disk_data_%s.vdi', "els01")
    #     els01.vm.network "private_network" , ip: "172.28.128.21"
    #     els01.vm.provider "virtualbox" do |v|
    #         v.cpus = 3
    #         v.memory = 2048
    #     end
    #end
    
end