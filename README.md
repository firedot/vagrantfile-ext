# vagrantfile-ext
Basic Vagrantfile

## Vagrantfile that downloads a box from the VagrantCloud, sets simple config, and installs nginx: 

````
#Line that configures hostname
config.vm.hostname = "bananas3"

#Line that installs nginx from script located ./scripts
config.vm.provision "shell", path: "./scripts/web.sh"

#Line that configures ip: 
config.vm.network "private_network", ip: "192.168.56.56"

#Line that configures firwarded port: 
config.vm.network "forwarded_port", guest: 80, host: 8080


````
