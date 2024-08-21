Bassic ( CPU, Network,Disk and status check), it will give every 5 mint logs,

Details - it will give every seconds logs

## Alarms have 3 States
Cloud Watch alarms are on single metrics
1. In Alarm - if CPU utiliztion is high, means if its 90% then it will return In Alarm
2. Ok Alarm - if CPU utilization is less then 90% tehn it will return Ok
3. Insuffienct - if EC2 instance is stopped state

## Composite Alarms
   Composite alarms are monitoring states of multiple alarms. have to use And or OR conditions
## Evemts

	![image](https://github.com/user-attachments/assets/e31e400e-6c95-40d2-9b1a-cf0663f53e04)

## Cannaries 
   will be used for Application logs 
   
## x-Ray
   it will captured Request and Respose of the application
   
## logs:

	- we have to install cloud watch agent in all application EC2 instances.
	- awscli.conf ---> contains region information
	- awslogs.conf ---> have appened out application log path
	- /var/log/messages
	- /var/log/tomcat
	- create IAM role and restart the agent 
cloudwatch logs have two types
1. LogGroup  - cloudwatch agent will push logs this file  
2. LogStreams - it will contain instance id

## install cloud agent

- yum install -y awslogs

- cd /etc/awslogs

- **vi awscli.conf**   -- updated region

- vi awslogs.confg
  
    file= specify application path
  
    log_stream_name= {ec2 instanceid}

     log_group_name=  group name

  - systemctl start **awslogsd**

**Difference  between Cloudwatch and CloudTrail**

**Cloudwatch** - is used to capture Application logs and Sysemlogs ( CPU, Network,Disk, status check and memory like)

**Cloud Trail** -  is used to capture resource level logs, it captures detailed information about API calls made to AWS services, including who made the call, what actions were performed, and when they occurred.


#### 	----------------								Cloud Trails --------------------------------

by default it will have 90 days logs , if you want more than that , we hvae to create  Trail and it will ** not caputure online logs**.

Cloud Trails are 3 types

1. Managment Trails - one managment is free, will store in S3 bucket ( in zip format) or Cloudwatch ( have to create logs group, role and policy) // just have to check box 
      
	it will capture all activites of AWS Console like resource creation , deletion and modification etc.
	
2. Data event 

	it will capture logs  inside resource. what changes happend at S3 bucket level like what file added , what changes happened in the data level. its support S3 bucket, lake formaton , SNS , lamda, dynamodb and etc
	
	
3. Insight events - it will capture all unsual activites in AWS accounts



### 	--------------							Config  ----------------------------------------------


AWS Config will run along with cloud trail and store logs in S3 bucket. we have to enable this servierce.

it will monitor all resources in the particular region. it will caprtue what changes and at what time changes happened.

it will collect details from cloud trail.

we capture details of specific resource out of multipule resource or all resources. 

it will capture all global resource logs like S3 , IAM etc  logs.

Also we can set the rules at resource level. if any one  made changes at resouce level (public access)  it will trite it as non-complaint and trigger imidetaily SNS notification.


----------
EC2
CloudWatch
EBS
S3
EFX
DynomoDB
Mongodb
Redies
casandra
SQL
Cloudwatch- failover
RDS
batch
