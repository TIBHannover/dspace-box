# -*- mode: python -*- 
# vi: set ft=python : 

VAGRANTFILE_API_VERSION = "2" 

Vagrant.configure("2") do |config|



  config.vm.define "dspace-vm-77" do |srv|
    srv.vm.box = "debian/buster64"
    srv.ssh.insert_key = false
    srv.vm.hostname = "dspace.box"
    srv.vm.network :private_network, ip: "192.168.98.111"

    srv.vm.provider :virtualbox do |vb| 
      vb.name = "dspace"
      vb.memory = 8048
      vb.cpus = 2
    end

 
  end

  
  
  config.vm.provision :ansible_local do |ansible|

    ansible.install = true
    # ansible.become = true
    ansible.compatibility_mode = "2.0"
    ansible.install_mode = "pip_args_only"
    ansible.pip_install_cmd = "sudo apt-get install -y python3-distutils && curl -s https://bootstrap.pypa.io/get-pip.py | sudo python3"
    ansible.pip_args = "ansible-core==2.11.8"
    ansible.verbose = true
    ansible.playbook = "ansible/playbook.yml"
    ansible.galaxy_role_file = "requirements.yml"
    ansible.extra_vars = { ansible_python_interpreter:"/usr/bin/python3" }
  end

  # config.vm.synced_folder ".", "/vagrant"

  
end  
