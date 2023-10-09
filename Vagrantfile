

Vagrant.configure("2") do |config|

  config.vm.define "dspace-vm" do |srv|
    srv.vm.box = "debian/bookworm64"
    srv.ssh.insert_key = false
    srv.vm.hostname = "dspace.box"
    srv.vm.network :private_network, ip: "192.168.56.111"

    srv.vm.provider :virtualbox do |vb| 
      vb.name = "dspace-vm"
      vb.memory = 8048
      vb.cpus = 2
    end
 
  end

  config.vm.provision :ansible_local do |ansible|
    ansible.install = true
    ansible.version = "latest"
    ansible.compatibility_mode = "2.0"
    ansible.verbose = true
    ansible.playbook = "ansible/playbook.yml"
    ansible.galaxy_role_file = "requirements.yml"
  end
end
