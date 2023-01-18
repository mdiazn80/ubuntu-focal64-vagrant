Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/focal64"

    config.ssh.forward_agent="true"
    config.ssh.forward_x11="true"

    # config.vm.network "forwarded_port", guest: 8834, host: 8834
    config.vm.network "forwarded_port", guest: 80, host: 8080
    config.vm.network "forwarded_port", guest: 3306, host: 3306

    config.vm.synced_folder "./data", "/vagrant"

    config.vbguest.auto_update = false
    config.vbguest.no_remote = true

    # VirtualBox specific settings
    config.vm.provider "virtualbox" do |vb|
        vb.gui = false
        vb.cpus = 4
        vb.memory = "8192"
    end

end