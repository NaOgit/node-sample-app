required_plugins = ["vagrant-hostsupdater"]

required_plugins.each do |plugin|
  exec "vagrant plugin install #{plugin}" unless Vagrant.has_plugin? plugin
end

Vagrant.configure("2") do |config|
# 2 is the version we're using
# Use vagrant to build virtual machine on everyone else's machine
# Virtual box will look after it

config.vm.box = "ubuntu/xenial64"
config.vm.network("private_network", ip: "192.168.10.100")
config.hostsupdater.aliases = ["development.local"]
# When this line is executed, it knows if you go to development.local, it will go to the ip address above

# Concatonate = cat
# config.vm.box_check_update = false

end
