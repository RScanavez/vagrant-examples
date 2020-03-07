Vagrant.configure("2") do |config|
  config.vm.define "webserver" do |webserver|
   webserver.vm.box = "ubuntu/trusty64"
   webserver.vm.synced_folder "site", "/var/www/html"
   webserver.vm.network "forwarded_port", guest:80, host:8080
   webserver.vm.provision "shell" do |shell|
    shell.inline = "apt-get update -y"
    shell.inline = "apt-get install apache2 -y"
    end
  end 
end
