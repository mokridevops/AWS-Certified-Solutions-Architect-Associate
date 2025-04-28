
# Day1: 

Tour of AWS Console & Services in AWS


# IAM Permissions:

![image](https://github.com/user-attachments/assets/c29cba45-7ca2-4025-9c1a-8b76486f4c8f)


![image](https://github.com/user-attachments/assets/bbeff65b-2904-4d64-8751-6e40bbf91274)


IAM is not region specific, it is available globally.

![image](https://github.com/user-attachments/assets/e0c5896c-9b12-4947-b2c6-edd4b32fbd3b)


Why do we create users:  by default we are - a root user - it is not best practice to give access to root user - the root user can delete the resources.

![image](https://github.com/user-attachments/assets/dea90a8c-b4df-481a-a01a-6d3e5fe8b5f8)

this is a root user

lets create - users in IAM


# IAM Policies Inheritance


![image](https://github.com/user-attachments/assets/15f23bb4-b810-418f-b008-b70204489b72)


![image](https://github.com/user-attachments/assets/12a1c5db-3ec0-4f47-8d93-2334540aaaf7)


Sample JSON structure for IAM policy:

{
   "Version": "2012-1-17",
   "Id": "S3-Account-Permissions",
   "Statement":  [
   {
      "Sid": "1",
      "Effect": "Allow",
      "Principal": {
      "AWS": ["arn:aws:iam::1234445555:root"]
    },
    "Action": [
    "s3:GetObject",
    "s3:PutObject"
    ],
    "Resource":["arn:aws:s3:::mybucket/*"]
    }
  ]
 }

 


