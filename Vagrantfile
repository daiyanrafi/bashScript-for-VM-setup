# For jenkins setup

Vagrant.configure("2") do |config|
  config.vm.define "jenkins" do |jenkins|
    jenkins.vm.box = "geerlingguy/ubuntu2004"
    jenkins.vm.network "private_network", ip: "192.168.10.12"
    jenkins.vm.provider "virtualbox" do |vb|
      vb.memory = "2560"
      vb.cpus = 2 # Set the number of CPUs
    end # Add this line to close the vb block

    # Provisioner to run the shell script
    jenkins.vm.provision "shell", path: "E:/vagrant-vms/jenkins/jenkins.sh"
  end # Add this line to close the jenkins block
end # Add this line to close the config block
