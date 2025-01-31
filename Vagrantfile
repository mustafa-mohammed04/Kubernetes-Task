## Create Vagrantfile that depends on libvirt

``` bash
VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Specify the box to use
  config.vm.box = "generic/ubuntu2204"

  # Set the VM hostname
  config.vm.hostname = "Master.local"

  # Configure a public network with a static IP using the correct interface
  config.vm.network "public_network",
    ip: "192.168.1.99",
    dev: "wlo1",   # Use your active WiFi interface
    mode: "bridge" # Bridge mode for direct network access

  # Provider-specific configuration for Libvirt
  config.vm.provider :libvirt do |libvirt|
    libvirt.memory = 2048         # Set memory to 2GB
    libvirt.cpus = 2              # Allocate 2 CPUs
    libvirt.disk_bus = "virtio"   # Use virtio for better disk performance
  end
end

```

## Check Vagrant

vagrant validate


## Run Vagrantfile

vagrant up
vagrant status


## Remote 

vagrant ssh
```
