# work-on-WSL-note

install/uninstall
```
lxrun /install /y
lxrun /uninstall /full
```
update ubuntu version
```
sudo do-release-upgrade
```

## All Docker thing

### Set dockerhost

Expose your docker deamon in window docker-ce
```
$ echo “export DOCKER_HOST=localhost:2375” >> ~/.bashrc
```

### docker-compose wrong volumn mount in WSL

sudo vim /etc/wsl.conf

```
# Now make it look like this and save the file when you're done:
[automount]
root = /
options = "metadata"
```
then restart you computer
`df -h` you should see `mnt/c` to `/c`
