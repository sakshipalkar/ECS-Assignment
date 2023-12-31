1.Configure aws credential

2.Install aws cli version 2

3.Clone open-source github project.

4.Create EGR Public Repository by using repo.yaml.

5.You will see the below commands to push your docker image to the ECR repository

6.docker build -t sample_ecs .

7.docker tag sample_ecs public.ecr.aws/w0f5g4k6/deploy:v7'

8.aws ecr-public get-login-password --region us-east-1 | docker login --username AWS -p $(aws ecr get-login-password --region us-east-1)

9.docker push public.ecr.aws/w0f5g4k6/deploy:v7

10.Now create ECS Cluster by using cluster.yaml, it will create cluster in your AWS ECS

11.create IAM Role to create taskdefination by using taskexecution.yaml

12.create VPC and subnets using vpc.yaml

13.create taskdefination under which you can run your container, using tase.yaml
