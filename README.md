# work-on-WSL-note

install/uninstall
```
lxrun /install /y
lxrun /uninstall /full
```
update ubuntu version
+ do release-upgrade need `-d` to get newest images if not you will get ubuntu 16 instend of 18
+ if not you will find docker version problem
```
lsb_release -a
sudo do-release-upgrade -d
```

## All Docker thing

### Set dockerhost

+ Expose your docker deamon in window docker-ce (careful with bash profile)
+ you can't `docker ps` because in WSL we don't have images or container we have it at window so you need to expose it at window and tell WSL where it is

```
$ echo “export DOCKER_HOST=localhost:2375” >> ~/.bashrc
```

### docker-compose wrong volumn mount in WSL

+ docker relative path is broken you it don't know that `/mnt/c` is `/c` you need to tell them
+ you need `sudo vim /etc/wsl.conf`
+ `df -h` you should see `mnt/c` to `/c`

```
# Now make it look like this and save the file when you're done:
[automount]
root = /
options = "metadata"
```
then restart you computer
