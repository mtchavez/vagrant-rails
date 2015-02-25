# Vagrant Rails Dev Box

[![Latest Version](http://img.shields.io/github/release/mtchavez/vagrant-rails.svg?style=flat-square)](https://github.com/mtchavez/vagrant-rails/releases)

Simple Rails Dev box setup to provision with Vagrant and push new
versions to Atlas to be used in other projects.

## Requirements

* Ansible is required for provisioning
  * Install via `pip install -r requirements.txt`
* Vagrant
* Virtualbox

## Rails Setup

* RVM - Ruby 2.2.0
* NodeJS - version 0.10.26
* Postgres - version 9.3
* Memcached
* Redis
* CoffeeScript
* PhantomJS

## Atlas Vagrant Box

Versions of the box will be hosted on Atlas to be used in other projects.
A simple Vagrant file using the box would be:

```ruby
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = 'mtchavez/rails-dev'
  config.vm.box_version = '>=0.0.1'
end
```
