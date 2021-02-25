# MacOS --> ubuntu: use XQuartz application command line to ssh in with vagrant ssh

Vagrant.configure(2) do |config|
  config.vm.box ="ubuntu/bionic64"
  config.vm.network "forwarded_port", guest: 2020, host: 2020
  
  ### uncomment the following line and replace [ABSOLUTE_PATH] with the absolute path on your system
  # config.vm.synced_folder "[ABSOLUTE_PATH]/MathInspector", "/MathInspector"
  
  config.vm.provision :shell, :path => "install.sh"
  config.ssh.forward_x11 = true
end