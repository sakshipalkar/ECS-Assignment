1.Configure aws credential

2.Install aws cli version 2

3.Clone open-source github project.

4.Create EGR Public Repository by using repo.yaml.

5.You will see the below commands to push your docker image to the ECR repository

6.docker build -t sample_ecs .

7.docker tag sample_ecs public.ecr.aws/w0f5g4k6/deploy:v7'

8.aws ecr-public get-login-password --region us-east-1 | docker login --username AWS -p $(aws ecr get-login-password --region us-east-1)

9.docker push public.ecr.aws/w0f5g4k6/deploy:v7

10.Now create ECS Cluster and load balancer by using loadbalancer.yaml, it will create ECS Cluster as well as load balancer in your AWS cloud 

11.create IAM Role to create ECS Task execution role by using Taskexecution.yaml

12.create VPC and subnets using vpc.yaml

13.create taskdefination and service through which you can run your container, using ECS_Service.yaml

14.To Monitore CPU & Memory Utilization set alaram for the same by using Dashboard_Alarm.yaml

15.To get Notification for the alarm SNS topic need to be subscribed.

16.To Access or to check web application running or not use public IP address of the task as above web application expose on port 8000.


