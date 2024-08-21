Bassic ( CPU, Network,Disk and status check), it will give every 5 mint logs,

Details - it will give every seconds logs

## Alarms have 3 States
Cloud Watch alarms are on single metrics
1. In Alarm - if CPU utiliztion is high, means if its 90% then it will return In Alarm
2. Ok Alarm - if CPU utilization is less then 90% tehn it will return Ok
3. Insuffienct - if EC2 instance is stopped state

## Composite Alarms
   Composite alarms are monitoring states of multiple alarms. have to use And or OR conditions
 
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

yum install -y awslogs

cd /etc/awslogs
vi awscli.conf   -- updated region
vi awslogs.confg 
    file= specify application path
	log_stream_name= {ec2 instanceid}
	log_group_name=  group name

systemctl start **awslogsd**

**Difference  between Cloudwatch and CloudTrail**

**Cloudwatch** - is used to capture Application logs and Sysemlogs ( CPU, Network,Disk, status check and memory like)

**Cloud Trail** -  is used to capture resource level logs, it captures detailed information about API calls made to AWS services, including who made the call, what actions were performed, and when they occurred.






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
