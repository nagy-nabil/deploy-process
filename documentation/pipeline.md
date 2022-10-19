## piplLine [ci/cd]
using **CircleCI** to automate deploying process, check out the configuration [.circleci/config.yml](/.circleci/config.yml).

our pipeline contain two jobs
- **test-build**
    - starts with install **node.js** and install **chrome** for ui testing 
    - install Front-end dependencies
    - install Back-end dependencies
    - Lint Front-end make sure the code use fixed way to construct the app accross code base
    - Test Front-end make sure new added features didn't destroy any working one and in general make sure the app working as expected
    - Build Front-end to make sure our App build without any errors
    - Build Back-end to make sure our App build without any errors
- **pipeline waits for manual approval to deploy**
- **deploy**
    - install **node.js**
    - setup **eb cli**
    - setup **aws cli**
    - run deploy front-end from the main **[packeage.json](/package.json)**
    - run deploy back-end from the main **[packeage.json](/package.json)**


**screenshot for Build pipeline**
![build pipe](/assets/build_pipe.png)

**screenshot for manual deploy approval**
![build pipe](/assets/manual_approval.png)

**screenshot for Deploy pipeline**
![build pipe](/assets/deploy_pipe.png)

**screenshot for S3 Bucket for static hosting**

![RDS](/assets/s3Healty.png)

**screenshot for S3 Bucket for api media**

![RDS](/assets/mediaBucket.png)
