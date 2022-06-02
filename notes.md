## Steps:

* Deploying the Application

    1. Connect Postgres Database locally

    2. Check that it works locally

    3. Create AWS RDS account

    4. Whitelist inbound traffic sources (VPC) to coonect to AWS DB

    5. Check DB connection with Postbird

    6. Create S3 Bucket

    7. Create IAM dashboard

    8. Upload Static Files to S3 Bucket: ``` aws s3 cp --recursive --acl public-read ./www s3://tasnim-udagram/ ```

    9. Initialize elastic beanstalk application: ``` eb init udagram-api --platform node.js --region us-east-1 ```

    10. Create elastic beanstalk environment: ``` eb create --sample udagram-api-dev ```

    11. Make sure we are using the environment: ``` eb use udagram-api-dev ```

    12. Build our project

    13. Archiving & uploading built project

    14. Writing ``` deploy:artifact: www/Archive.zip``` in config.yml in .elasticbeanstalk

    15. deploy the project: ``` eb deploy udagram-api-dev ```

    16. Writing project-level package.json

* Creating a Pipeline
    1. Writing .circleci/config.yml
    2. Connect circleci with github


## Used Commands:

1. aws s3 cp --recursive --acl public-read ./www s3://tasnim-udagram/

2. eb init udagram-api --platform node.js --region us-east-1

3. eb create --sample udagram-api-dev

4. eb use udagram-api-dev

5. eb deploy udagram-api-dev

6. eb open

7. eb terminate


## Error Notes:

1. Change .env variables from local to aws services

2. upgrade front end versions

3. udagram-qpi/package.json: change main: **src/server.js** to main: **www/server.js**

4. udagram-frontend/src/environments/environment.prod.ts >> change api host to aws elastic beastalk host

5. Enable ACL from E3/permissions/Object Ownership to upload statis files successfully


