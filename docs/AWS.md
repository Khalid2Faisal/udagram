# AWS Services

## Udagram Application System Diagram
the diagram below shows the system architecture of the Udagram application.
<br>

![Udagram Application System Diagram](./media/udagram%20system.png)

---

## S3 Bucket
s3 bucket is used to host the frontend of the application. The bucket is configured to be publicly available.

### permissions screenshot
![s3 bucket permissions](./media/s3%20permissions.png)


### Bucket Policy
The bucket policy is configured to allow public access to the bucket.

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::my-udagram/*"
        }
    ]
}
```

---

## Elastic Beanstalk
Elastic Beanstalk is used to deploy the backend of the application. It is a `nodejs` application.

### configuration
the application is configured to use the `nodejs` platform and the `64bit Amazon Linux 2 v4.1.0 running Node.js` environment.
![elastic beanstalk configuration](./media/elastic%20beanstalk%20config.png)

### app
![elastic beanstalk app](./media/elastic%20beanstalk%20app.png)

### environment health
The environment health is `Green`.
![elastic beanstalk environment health](./media/elastic%20beanstalk%20health%20.png)

---

## RDS
RDS is used to host the database of the application. It is a `PostgreSQL` database.

### configuration
The database is configured to be publicly available.
![RDS configuration](./media/rds%20config.png)

### security group rules
The security group rules are configured to allow public access to the database.
![RDS security group rules](./media/rds%20security%20group%20rules.png)

### database health
The database health is `available`.
![RDS database health](./media/rds%20health.png)

---