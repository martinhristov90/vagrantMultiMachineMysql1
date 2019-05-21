## This repository provides a simple Vagrantfile to use with Vagrant, providing multi-machine setup, two of the machines provide nginx servers and one is MySQL server.

## How to install Vagrant :

- Information about installing Vagrant can be found on the official HashiCorp website [here](https://www.vagrantup.com/docs/installation/)

## How to use it :

- In a directory of your choice, clone the github repository with `git clone https://github.com/martinhristov90/vagrantMultiMachineMysql1.git`
- Change into the directory using : `cd vagrantMultiMachineMysql1`
- Execute `vagrant up`
- It might take some time to download the boxes since you do not have them added to Vagrant.
- Check with `vagrant status` that you have both Vagrant boxes running. The output should look like this:
```shell

Current machine states:

web1                      running (virtualbox)
web2                      running (virtualbox)
mysql                     running (virtualbox)

This environment represents multiple VMs. The VMs are all listed
above with their current state. For more information about a specific
VM, run `vagrant status NAME`.

```

- To view the hosted websites used this :

    - For "web1" connect to your local machine to address `localhost:8081`
    - For "web2" connect to your local machine to address `localhost:8082`


- To stop the running machines execute `vagrant halt`, to destroy the setup use `vagrant destroy`.

