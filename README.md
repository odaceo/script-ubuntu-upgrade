# Script | Ubuntu | Upgrade

[![License](https://img.shields.io/github/license/odaceo/script-ubuntu-upgrade.svg)](LICENSE)

## Description

Bash script for keeping your system up-to-date on Ubuntu.

## Provisioning Vagrant machine

To provision a Vagrant machine use the following ``Vagrantfile``:

``` shell
# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  config.vm.box = "ubuntu/xenial64"
  
  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  config.vm.provision "shell", privileged: false, 
    path: "https://raw.githubusercontent.com/odaceo/script-ubuntu-upgrade/xenial64/install.sh"
end
```

## Reporting Issues

Issues can be reported at [https://github.com/odaceo/script-ubuntu-upgrade/issues](https://github.com/odaceo/script-ubuntu-upgrade/issues)

## Source code

The source code is available at [https://github.com/odaceo/script-ubuntu-upgrade](https://github.com/odaceo/script-ubuntu-upgrade)

## License

All the source code is distributed under [ASL 2.0](LICENSE).

## Copyright

© 2016 [Odaceo](http://odaceo.ch). All rights reserved.