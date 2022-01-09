# Using vagrant for testing purposes
Vagrant.configure("2") do |config|
    config.vm.box = "generic/gentoo"
    config.ssh.insert_key = false

    config.vm.provision "ansible" do |ansible|
        ansible.verbose = "v"
        ansible.playbook = "main.yml"
    end

    config.vm.provider :libvirt do |domain|
        domain.qemu_use_session = false
    end
end
