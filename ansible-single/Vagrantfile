Vagrant.configure(2) do |config|

    # Set machine size
    config.vm.provider :libvirt do |domain|
        domain.memory = 2048
        domain.cpus = 1
    end

    # Tower/PgSQL machine
    config.vm.define "tower" do |tower|
        tower.vm.box = "centos/7"
    end

    # Ansible Tower configuration
    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbook.yaml"
    end

end
