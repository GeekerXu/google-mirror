# google-mirror
Google 镜像


1.docker 安装 

curl -sSL https://get.docker.com/ | sh 

2.创建dockerfile 目录 并进入目录 

mkdir -p /home/docker/dockerfile-google-mirror && cd /home/docker/dockerfile-google-mirror

3.下载dockerfile 文件

wget https://raw.githubusercontent.com/GeekerXu/google-mirror/master/dockerfile


4.创建镜像

docker build -t geekerxu/google-mirror:latest .

5.启动容器

docker run -d -p 80:80 --restart=always --name google-mirror geekerxu/google-mirror
