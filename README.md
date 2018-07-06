# work-on-WSL-note

##Set host
$ docker -H localhost:2375 images

If you don't want to type the host every time, you can set up and environment variable called DOCKER_HOST to localhost:2375

$ export DOCKER_HOST=localhost:2375

Now just running docker images will show the images in your host environment.

But, that environment variable will last only as long as the session does. You would have to set it every time you open bash. So, in order to avoid that, you set that variable in a file called .bash_profile in your home directory, like this:

$ echo “export DOCKER_HOST=localhost:2375” >> ~/.bash_profile


## docker-compose wrong mount in WSL
sudo vim /etc/wsl.conf

```
# Now make it look like this and save the file when you're done:
[automount]
root = /
options = "metadata"
```
then restart you computer
`df -h` you should see `mnt/c` to `/c`
