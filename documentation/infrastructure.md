## cloud infrastructure
our app use different aws cloud services to deploy differevnt parts of the application

![cloud infrastructure](/assets/cloud_infrastructure.png)

**RDS** used to deploy relational database, our application using postgreSQL so it was to obvious choice for the database

![RDS](/assets/RDS.png)

**Elastic Beanstalk Environments** are preconfigured server for deploying applications like python, node.js, so our application using it for deploying the server.

eb use other aws services under the hood like
    - EC2 for deploying server
    - S3 for storing code and then download it in the servers and run it
    - SNS Simple Notifaction system

![RDS](/assets/elasticbeanstalk.png)

**S3 Bucket** used for delpoying static files, our App use it to deploy front-end because it can be used for static hosting and can made public easy to be available for our clients.

![RDS](/assets/s3Healty.png)
