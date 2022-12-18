# ubuntu-docker

```sh
docker pull ubuntu:latest
docker images
docker run -it --name ubuntu -v E:\Dev\Ubuntu:/home ubuntu
```

```sh
docker start -i ubuntu
docker stop ubuntu
```

```sh
apt update && apt upgrade
apt install sudo
useradd -m flo
cat /etc/passwd
passwd flo
sudo usermod -a -G sudo flo
sudo -su flo
```

```sh
userdel -r flo
```
