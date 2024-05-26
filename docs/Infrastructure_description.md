# Infrastructure description

## Elasic Beanstalk
Elatic Beanstalk is used to hosting Nodejs Back-end - Udagram API
- Application name: udagram-be-duongntt1
- Ennviroment name: Udagram-be-duongntt1-env
- Domain: [Udagram-be-duongntt1-env.eba-srpm5jua.us-east-1.elasticbeanstalk.com](http://udagram-be-duongntt1-env.eba-srpm5jua.us-east-1.elasticbeanstalk.com/) 

- Platform: Node.js 14

## S3 bucket
S3 bucket is used to host the frontend files. 
- Bucket name: udagram-frontend-duongntt1 
- Region: us-east-1
- Public S3 bucket

## RDS database
RDS is used to create PostgresSQL database. It is used to store user metadata. 
- Instance name: duongntt1-udagram-db

## Connect flow
1. User access static website hosted by S3 bucket (Frontend) then Input data.
2. S3 bucket receive data and send it to Elastic Beanstalk application (Back-end) by HTTP request.
3. Backe-end (Elastic Beanstalk) save data to database (RDS).