# pardus-install

- install docker:
```bash
apt-get update
apt-get install -y \
     apt-transport-https \
     ca-certificates \
     curl \
     gnupg2 \
     software-properties-common
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
apt-key list | grep -B2 docker
apt-key fingerprint 0EBFCD88
sudo add-apt-repository \
    "deb [arch=amd64] https://download.docker.com/linux/debian \
    buster \
    stable"
apt-get update
apt-get install -y docker-ce docker-ce-cli containerd.io
systemctl start docker
systemctl enable docker
docker ps
```
```bash
debootstrap ondokuz ondokuz http://depo.pardus.org.tr/pardus
```
