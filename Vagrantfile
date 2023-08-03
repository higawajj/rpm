# -*- mode: ruby -*- 
# vi: set ft=ruby : vsa
Vagrant.configure(2) do |config| 
  config.vm.box = "centos/7" 
  config.vm.box_version = "2004.01"
  config.vm.synced_folder './sync', '/vagrant', disabled: true
  config.vbguest.auto_update = false  
  config.vm.provider "virtualbox" do |vb| 
    vb.customize ["modifyvm", :id, "--memory", "1024"] 
  end
  config.vm.define "rpm" do |rpm|
    rpm.vm.hostname = "rpm"
    rpm.vm.provision "shell", path: "rpm_script.sh"
  end 
end 
 