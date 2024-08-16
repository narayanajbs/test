## KMS Documents

https://www.youtube.com/watch?v=8ailVnVPigk&t=3332s

There are 3 types of keys
1. AWS Managed Keys
2. Customer Managed Keys
3. AWs Owned Keys
![image](https://github.com/user-attachments/assets/ba13e312-a3b6-403c-a8d4-127dfffead3a)

### commands
#### generte data key
aws kms generate-data-key --key-id alias/app1key --key-spec AES_256



 {
            "Sid": "Enable IAM User Permissions",
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::381492151298:root"
            },
            "Action": "kms:*",
            "Resource": "*"
        },
		
### Alias 

Each resouce can have multiple alias
Alias are 2 types

1. Kms:RequestAlias --  it will fetch all alias which start with APP ( based on the wild charector)
	
	"condition" : {
		"StringLike" :{
			"kws:RequestAliases" : "alias/App*"
			}
	} 
2. KMS:ResourceAlias- this will filter based on the resource name.

	Policy conditions
	
    1. if any alias name match with keyword "App*" , it will have premission to execute all alias in that particular resources.
		
		"condition" : {
			"ForAnyVlue:StringLike" :{
				"kws:ResourceAliases" : "alias/App*"
				}
		} 
		
	2. if any alias name not match with keyword "App*"  in that particular resource, it will skip to execute that particular resources.
		
		"condition" : {
			"ForAllVlue:StringLike" :{
				"kws:ResourceAliases" : "alias/App*"
				}
		} 
		
		