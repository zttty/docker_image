# python-ssh

1. build this python docker image with ssh

   `docker build -t python-ssh:v1 .`

2. mapping code folder into container and we could ssh to this container and connect it  to debug remotely

   `docker run -idt --name bd -v ./code:/code python-ssh:v1`

