Execute the following command to have the "Jenkins with Docker" image spun up
-----------------------------------------------------------------------------

docker run -it -p 8080:8080 -p 50000:50000 \
    -v jenkins_home:/var/jenkins_home \
    -v /var/run/docker.sock:/var/run/docker.sock \
    --restart unless-stopped \
    4oh4/jenkins-docker



Connect to the container with the console (CL)
----------------------------------------------

You're logged as the user "Jenkins" --> change the user to "root" (su - user)



Install docker-compose (change version number in the CL)
--------------------------------------------------------

curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

chmod +x /usr/local/bin/docker-compose
