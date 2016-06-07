# Learning Locker in a Docker container

Created by Andrew Blum @ Red Hat and updated by Matt Perkins. 
https://github.com/LearningLocker/docs/issues/15

Start with `docker run -d -p 8080:80 [image]`

# Note for AWS

The Dockerfile and llstart up scripts have been tweaked to run in the free Amazon Linux container provided by AWS. Storage space is limited, so the smallfiles flag was added. To enable data persistance, you need to create a data folder in the AWS user root and map that to the MongoDB in the Docker image. In my case, this folder was named `db`.

Start with `docker run -v /home/ec2-user/db:/data/db -p 80:80 [image]`
