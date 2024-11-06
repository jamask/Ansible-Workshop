Vagrant.configure("2") do |config|
      config.vm.box = "ubuntu/focal64"
      config.vm.hostname = "controlnode"
      config.vm.network "private_network", ip: "192.168.56.2"
      config.vm.provision "shell", inline: <<-SHELL
        sed -i 's/ChallengeResponseAuthentication no/ChallengeResponseAuthentication yes/#g' /etc/ssh/sshd_config
        service ssh restart
      SHELL
    end
