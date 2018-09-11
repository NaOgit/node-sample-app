Vagrant.configure("2") do |config|
# 2 is the version we're using
# Use vagrant to build virtual machine on everyone else's machine
# Virtual box will look after it

config.vm.box = "ubuntu/xenial64"
config.vm.network("private_network", ip: "192.168.10.100")
config.hostsupdater.aliases = ["development.local"]
config.vm.box_check_update = false

end
