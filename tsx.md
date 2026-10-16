ssh-keygen -t ed25519

ssh root@163.223.9.81

mkdir -p ~/.ssh

chmod 700 ~/.ssh

nano ~/.ssh/authorized_keys

chmod 600 ~/.ssh/authorized_keys

adduser phamthihongnhung-cntt4

usermod -aG sudo phamthihongnhung-cntt4
exit

ssh phamthihongnhung-cntt4@221.121.4.10
mkdir -p /home/phamthihongnhung-cntt4/.ssh

sudo chown -R phamthihongnhung-cntt4:phamthihongnhung-cntt4 /home/phamthihongnhung-cntt4/.ssh

nano /home/phamthihongnhung-cntt4/.ssh/authorized_keys

sudo chmod 600 /home/phamthihongnhung-cntt4/.ssh/authorized_keys

sudo apt update && sudo apt -y upgrade

sudo apt-get update
(chạy tới đây thì đẩy git lên) -> nhập đẩy 3 cái post -> chạy hết các lệnh còn lại cho tới docker --verson

sudo apt-get install -y ca-certificates curl gnupg

sudo install -m 0755 -d /etc/apt/keyrings

sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc

sudo chmod a+r /etc/apt/keyrings/docker.asc

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update

sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

sudo usermod -aG docker $USER

sudo systemctl enable --now docker

newgrp docker
// chạy tới đây rổi chụp 
docker --version
docker ps
