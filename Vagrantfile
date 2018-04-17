Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.provision "shell", :inline => <<-SHELL
    sudo rpm -Uvh https://yum.puppet.com/puppet5/puppet5-release-el-7.noarch.rpm
    yes | sudo yum -y install puppet-agent
  SHELL

  config.vm.provision "puppet" do |puppet|
    puppet.module_path = "modules"
  end
end
