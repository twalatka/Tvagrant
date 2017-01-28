Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.synced_folder ".", "/var/www/project"
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y g++
    curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
    sudo apt-get install -y nodejs
  SHELL
end
