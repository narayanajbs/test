

## AutoScalling Health checks

#### Turn on Elastic Load Balancing health checks ( check box)

	Elastic Load Balancing monitors whether instances are available to handle requests. When it reports an unhealthy instance, EC2 Auto Scaling can replace it on its next periodic check.

#### Turn on Amazon EBS health checks ( checkbox)
EBS monitors whether an instance's root volume or attached volume stalls. When it reports an unhealthy volume, EC2 Auto Scaling can replace the instance on its next periodic health check


	default -300 sec


## Enable instance scale-in protection ( checkbox)

## Autoscalling Policies are 3 types
----------------
	Dynamic scalling policies
	Predictive scalling policies
	scheduled actions

## Dynamic scalling policies Types 
-------------
1. Target trackign scalling
2. step scalling
3. simple scalling


IMP -- autoscalling always create instance (scaling up instance) from launch template not from running instance


To set the alarm for autoscalling
----------------
1. install aws cli
2. login with screate key and id
3. execute below commands
    set-alarm-state
	--alarm-name <value>
	--state-value <value>
	--state-reason <value>
	
	example
	
	    set-alarm-state
	--alarm-name satyacpuut
	--state-value ALARM
	--state-reason "can give any name"
	


## ------------------------------ Route53 Health Check -------------------------------------------

1. Endpoint Health Check
2. Calculated Health Check
3. Health Check based on a Cloudwatch Alaram.

   ![image](https://github.com/user-attachments/assets/1a1d6f37-e0e9-4a64-93c3-bfd2fbe834c1)
