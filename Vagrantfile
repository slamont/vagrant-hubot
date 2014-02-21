# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.define "irc" do |irc|
#    irc.vm.provision "shell",
#      inline: "echo FOO"
    irc.vm.provision "puppet" do |puppet|
      puppet.manifest_file = "irc.pp"
      puppet.module_path = "modules"
    end  end

  config.vm.define "bot" do |bot|
#    bot.vm.provision "shell",
#      inline: "echo BAR"
    bot.vm.provision "puppet" do |puppet|
      puppet.manifest_file = "bot.pp"
      puppet.module_path = "modules"
    end
  end

end
