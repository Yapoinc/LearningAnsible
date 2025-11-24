
Install openssh-server (allow the connection via ssh)
sudo apt update
sudo apt install openssh-server -y

sudo systemctl start ssh
sudo systemctl enable ssh (on reboot start the service)
