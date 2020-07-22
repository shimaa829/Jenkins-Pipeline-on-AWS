# Jenkins-Pipeline-on-AWS

In this project,I create and run an instance on AWS, configure Jenkins, and create a pipeline to deploy a static website on S3.

## Steps:

*  A new user with EC2 and S3 access is created that is not the root/admin user in AWS.

![alt text](https://github.com/shimaa829/Jenkins-Pipeline-on-AWS/blob/master/screenshots/screenshot-01.png)

*  An Ubuntu 18.04 t2.micro is launched and can be accessed via SSH using the PEM file.

![alt text](https://github.com/shimaa829/Jenkins-Pipeline-on-AWS/blob/master/screenshots/screenshot-02.png)

*  Jenkins is installed and running on Ubuntu EC2 , and The Jenkins instance can be reached over HTTP publicly troughs unique AWS URL.

![alt text](https://github.com/shimaa829/Jenkins-Pipeline-on-AWS/blob/master/screenshots/screenshot-03.png)

*  The ‘Blue Ocean’ plugin is installed.

![alt text](https://github.com/shimaa829/Jenkins-Pipeline-on-AWS/blob/master/screenshots/screenshot-04.png)

* The GitHub repository is added and shows in the BlueOcean dashboard, automatically recognizing the Jenkinsfile and setting up the initial pipeline that has 1 stage.

![alt text](https://github.com/shimaa829/Jenkins-Pipeline-on-AWS/blob/master/screenshots/screenshot-05.png)

*  The index.html file is published to the correct bucket in the right region, and the url is accessible via HTTP from anywhere.  

![alt text](https://github.com/shimaa829/Jenkins-Pipeline-on-AWS/blob/master/screenshots/screenshot-06.png)

*  A Jenkinsfile exists, that has the stages and steps defined that match how the pipeline looks in the Jenkins dashboard. For example ‘stage(‘Lint HTML’)’ should show as ‘Lint HTML’ in the pipeline. The AWS credentials and bucket name should all map to an existing S3 bucket that is publicly accessible and that it displays the contents of the index.html file.

![alt text](https://github.com/shimaa829/Jenkins-Pipeline-on-AWS/blob/master/screenshots/screenshot-08.png)

