Vagrant::Config.run do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  config.vm.define :misc do |misc_config|
       misc_config.ssh.max_tries = 100
       misc_config.vm.box = "Centos65"
       misc_config.vm.network :hostonly, "192.168.99.101"
       misc_config.vm.host_name = "misc"
       misc_config.vm.provision :puppet do |misc_puppet|
        misc_puppet.manifests_path = "manifests"
        misc_puppet.module_path = "modules"
        misc_puppet.manifest_file = "site.pp"
       end
   end  
end
