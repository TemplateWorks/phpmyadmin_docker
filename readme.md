## Remove Docker
--- 
sudo yum -y remove docker docker-client docker-client-latest docker-common docker-latest docker-latest-logrotate docker-logrotate docker-engine

## Install docker
---
curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

## Last command return error use
---

sudo yum install -y yum-utils

sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo

sudo yum install docker-ce docker-ce-cli containerd.io --allowerasing

## Install docker-compose
---
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose

## Install Git
---

sudo yum -y install git

## Clone phpmyadmin_docker repo
---

git clone https://github.com/TemplateWorks/phpmyadmin_docker.git
