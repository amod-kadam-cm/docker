# Welcome to the docker wiki!

The instructions provided are based on [https://docs.aws.amazon.com/AmazonECS/latest/developerguide/docker-basics.html#install_docker](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/docker-basics.html#install_docker)

Connect to ec2 server.

_Update the installed packages and package cache on your instance._

`sudo yum update -y`

Install the most recent Docker Community Edition package.
`sudo yum install -y docker`

Start the Docker service.
`sudo service docker start`

Add the ec2-user to the docker group so you can execute Docker commands without using sudo.

`sudo usermod -a -G docker ec2-user`

Log out and log back in again to pick up the new docker group permissions. You can accomplish this by closing your current SSH terminal window and reconnecting to your instance in a new one. Your new SSH session will have the appropriate docker group permissions.

Verify that the ec2-user can run Docker commands without sudo.

`docker info`
