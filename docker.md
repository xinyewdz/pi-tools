&01  docker安装
 1. 使用脚本安装
 ```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
 ```
 2. 使用仓库安装
 ```
 #安装仓库工具
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg2 \
    software-properties-common
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add - 
sudo apt-key fingerprint 0EBFCD88

#安装docker
sudo add-apt-repository \
   "deb [arch=arm64] https://download.docker.com/linux/debian \
   $(lsb_release -cs) \
   stable"
apt-get install docker-ce docker-ce-cli containerd.io

```

&02 配置文件
 docker配置文件 /etc/docker/daemon.json

 ```
{
    "data-root":"/data/docker_data",
    "registry-mirrors": ["https://xcjev1l7.mirror.aliyuncs.com"]
}

 ```

 #启动docker
 systemctl start docker