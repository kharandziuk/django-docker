# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

ENV['VAGRANT_DEFAULT_PROVIDER'] ||= 'docker'

Vagrant.configure("2") do |config|
  config.vm.define "app" do |app|
    app.vm.provider "docker" do |d|
      d.build_dir = "app_server/." #"phusion/baseimage"
      d.ports  = ['80:5000']
      #d.cmd = ["/sbin/my_init", "--enable-insecure-key"]
      #d.has_ssh = true
    end
    app.vm.synced_folder "./project/", "/opt/project/"
  end

  #config.ssh.username = "root"
  #config.ssh.private_key_path = "insecure_key"
end
