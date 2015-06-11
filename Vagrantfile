Vagrant.configure("2") do |config|
  config.vm.box = "centos6.5.3"
config.vm.box_url = "https://github.com/2creatives/vagrant-centos/" +
  "releases/download/v6.5.3/centos65-x86_64-20140116.box"
  config.vm.provider :virtualbox do |vb|
    vb.customize [ 'modifyvm', :id, '--memory', 1024 ]
  end
  config.vm.network "forwarded_port", guest: 3000, host: 6000

  config.vm.provision :shell, inline: "yum -y update"
  config.vm.provision :shell, inline: "yum -y install php php-cli php-common php-gd php-in tl php-mbstring php-mysql php-pdo httpd"

end
