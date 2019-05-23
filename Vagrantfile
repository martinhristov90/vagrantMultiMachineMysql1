Vagrant.configure("2") do |config|

    # our mysql box
    config.vm.define vm_name="mysql" do |node|
        node.vm.box = "martinhristov90/ubuntu_mysql"
        node.vm.hostname = vm_name
        node.vm.network "private_network", ip: "192.168.56.21"
        node.vm.synced_folder "db/", "/usr/local/db/", create: true
    end
    # end of mysql
    
    # we create a loop for web servers
    (1..2).each do |i|
        config.vm.define vm_name="web#{i}" do |node|
            node.vm.box = "martinhristov90/ubuntu_nginx"
            node.vm.hostname = vm_name
            node.vm.network "private_network", ip: "192.168.56.#{80 + i }"
            node.vm.network "forwarded_port", guest: 80, host: 8080 + i
            node.vm.synced_folder "www/", "/usr/share/html/www/", create: true
        end
    end
    # end of webserver
    
end
