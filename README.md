# This repo contains an Ember simple Hello World project.

## Prerequisites
- Install [Virtual box](https://www.virtualbox.org/wiki/Downloads)
- Install [Vagrant](https://www.vagrantup.com). For more information, visit [Vagrant Documentation](https://docs.vagrantup.com/v2/)
- Install [Packer](http://www.packer.io)
- Install [Terraform](https://www.terraform.io/)
## 

<img src="screenshots/diagram.png" width="720" height="405">


### How to use it
- clone the repo
```
git clone https://github.com/chavo1/hello-ember.git
cd hello-ember
vagrant up
```
## In order to build your custom Vagrant box you will need [THIS](https://github.com/chavo1/packer-vagrant-ember) GitHub repo.
## To deploy the project in AWS you should prepare an AWS custom AMI, please find it [HERE](https://github.com/chavo1/packer-ami-ember)
## The Terraform code to deploy in AWS is available [HERE](https://github.com/chavo1/terraform-ember-aws)
