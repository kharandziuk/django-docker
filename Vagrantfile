# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

ENV['VAGRANT_DEFAULT_PROVIDER'] ||= 'docker'

Vagrant.configure("2") do |config|
  config.vm.define "app" do |app|
    app.vm.provider "docker" do |d|
      d.build_dir = "." #"phusion/baseimage"
      d.ports  = ['80:5000']
    end
    app.vm.synced_folder "./project/", "/opt/project/"
  end

  #config.ssh.username = "root"
  #config.ssh.private_key_path = "insecure_key"
end
