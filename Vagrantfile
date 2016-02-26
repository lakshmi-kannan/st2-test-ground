# -*- mode: ruby -*-
# vi: set ft=ruby :

hostname = ENV['HOSTNAME'] ? ENV['HOSTNAME'] : 'st2test'

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    config.vm.network "public_network"
    config.vm.hostname = "#{hostname}"

    # sudo apt-get install curl
    # Needs sudo ./st2bootstrap-deb.sh
    config.vm.define "u14" do |u14|
      u14.vm.box = 'bento/ubuntu-14.04'
    end

    # DOESN'T WORK
    # sudo apt-get install curl
    # config.vm.define "u15" do |u15|
    #  u15.vm.box = 'bento/ubuntu-15.04'
    # end

    # Untested. No bootstrap script.
    config.vm.define "centos66" do |centos66|
      centos66.vm.box = 'puppetlabs/centos-6.6-64-nocm'
    end

    # Untested.
    config.vm.define "centos67" do |centos67|
      centos67.vm.box = 'bento/centos-6.7'
    end

    # sudo yum install wget (to download st2bootstrap-el7.sh)
    # sudo yum install net-tools (to get ifconfig)
    config.vm.define "centos7" do |centos7|
      centos7.vm.box = 'centos/7'
    end

    # sudo yum install wget (to download st2bootstrap-el7.sh)
    config.vm.define "centos71" do |centos71|
      centos71.vm.box = 'bento/centos-7.1'
    end

    config.vm.define "centos72" do |centos72|
      centos72.vm.box = 'bento/centos-7.2'
    end

    config.vm.provider :virtualbox do |vb|
      vb.name = "#{hostname}"
      vb.memory = 2048
      vb.cpus = 2
    end

    # Configure a private network
end
