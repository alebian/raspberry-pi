# Raspberry pi config

## SSH

To enable SSH run `sudo raspi-config`

```bash
echo '' >> ~/.bashrc
echo 'eval "$(ssh-agent -s)"' >> ~/.bashrc
```

## Install programs

### Miscellaneous

```bash
sudo apt install -y \
  vim \
  git \
  curl
```

### Docker

```bash
sudo apt-get install -y curl libffi-dev libssl-dev python3-dev python3 python3-pip

curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh

sudo usermod -aG docker pi

sudo pip3 -v install docker-compose
```
