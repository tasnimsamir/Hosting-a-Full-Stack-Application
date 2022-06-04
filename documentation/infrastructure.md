# Infrastructure Description

![Architecture](architecture_diagram.png)


Project Infrastructure consists of three main components as shown in above figure:

1. AWS RDS Postgres: database to store and retrieve data 

    URL: ``` postgres://postgres:Password123$@database-2.cf8kg2nkreyv.us-east-1.rds.amazonaws.com/postgres ```

2. AWS Elastic Beanstalk: acts as a srever

    URL: ```  udagram-api-dev.eba-m7rmmhm3.us-east-1.elasticbeanstalk.com ```

3. AWS S3: for static files storage (like frontend files)
    * Endusers can access the application through S3 Bucket.
    * URL:  http://tasnim-udagram.s3-website-us-east-1.amazonaws.com 
