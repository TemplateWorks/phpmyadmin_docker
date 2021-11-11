## Use this command to install dependencies

sudo yum install docker

sudo yum install git

sudo dnf config-manager --add-repo=https://download.docker.com/linux/centos/docker-ce.repo

sudo dnf install docker-ce docker-ce-cli containerd.io --allowerasing

systemctl enable --now docker

firewall-cmd --zone=public --add-masquerade --permanent
firewall-cmd --reload

sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

sudo usermod -aG docker student

git clone https://github.com/TemplateWorks/phpmyadmin_docker.git

cd phpmyadmin_docker/

sudo docker-compose up --build -d

