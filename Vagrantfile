Vagrant.configure("2") do |config|
    (1..2).each do |i|
      config.vm.define vm_name="web#{i}" do |node|
        node.vm.box = "martinhristov90/ubuntu_nginx"
        node.vm.hostname = vm_name
        node.vm.network "forwarded_port", guest: 80, host: 8080 + i

    end
    end

    config.vm.define vm_name="mysql" do |node|
        node.vm.box = "martinhristov90/ubuntu_mysql"
        node.vm.hostname = vm_name
    end
end
