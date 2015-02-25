# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = 'ubuntu/trusty64'
  config.vm.hostname = 'vagrant-rails'

  # Virtualbox VM config
  config.vm.provider 'virtualbox' do |vb|
    vb.name = 'vag-rails'
    vb.memory = '4096'
    vb.cpus = 2
    opts = ['modifyvm', :id, '--natdnshostresolver1', 'on']
    vb.customize opts
  end

  # Ansible provisioning
  config.vm.provision 'ansible' do |ansible|
    ansible.sudo = true
    ansible.playbook = 'ansible/vagrant.yml'
  end

  # Atlas box config
  config.push.define 'atlas' do |push|
    push.app = 'mtchavez/rails-dev'
  end
end
