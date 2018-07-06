# #bash

```
cp .bash_profile ~/.bash_profile
```

## git

```bash
git config --global alias.st status 
git config --global alias.cm 'commit -m'

git config --global core.excludesfile '~/.gitignore_global'
cp .gitignore_global ~/.gitignore_global
git config --global push.default simple
```

## docker thing

```bash
curl -fsSL get.docker.com -o get-docker.sh
sh get-docker.sh

curl -L https://github.com/docker/compose/releases/download/1.21.2/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
docker-compose --version
```
docker mount
```
cp wsl.conf /etc/wsl.conf
```