# aws-cli-docker
Ubuntu AWS CLI Version 2 Docker image

This image provides the AWS CLI in ubuntu. Please refer [AWS](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-docker.html) for a detailed documentation. 

## Install

You can install this by cloning the repository and running the below command in the same directory

``` bash
docker build -t awscliv2 .
docker run -it -d --name awscli awscliv2
```

If you want to share any host directory with the container then you can use the below command

```
docker run -it -d --name awscli -v /path/of/host/directory:/path/of/container/directory awscliv2
```

You can start and stop the container by using the below commands

```
docker start awscli
docker stop awscli
```

## Configuring AWS Cli

You can bash into the container and configure the AWS credentials.

```
docker exec -it awscli /bin/bash
```
Then from within container:

```
aws configure
```
