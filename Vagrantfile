# For JENKINS setup

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

# For NEXUS setup

config.vm.define "nexus" do |nexus|
  nexus.vm.box = "geerlingguy/centos7"
  nexus.vm.network "private_network", ip: "192.168.10.13"
  nexus.vm.provider "virtualbox" do |vb|
    vb.memory = "2560"
    vb.cpus = 2 # Set the number of CPUs
  end # Add this line to close the vb block

  # Provisioner to run the shell script
  nexus.vm.provision "shell", path: "E:/vagrant-vms/nexus/nexus.sh"
end # Add this line to close the nexus block
end # Add this line to close the config block

# For SONARQUBE, NGINX, POSTGRESQL setup

config.vm.define "sonarqube" do |sonarqube|
  sonarqube.vm.box = "geerlingguy/ubuntu2004"
  sonarqube.vm.network "private_network", ip: "192.168.10.15"
  sonarqube.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
    vb.cpus = 4 # Set the number of CPUs
  end

  sonarqube.vm.boot_timeout = 250 # Set the boot timeout

  # Provisioner to run the shell script
  sonarqube.vm.provision "shell", path: "E:/vagrant-vms/sonarqube/sonar-setup.sh"
end
end