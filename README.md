# Simple PHP Application

## Team members:
- Williams Osunkwo
- Reina Vencer
- Chai Narukulla
- Paula Thomas

## Deployed Link:
[Deployed PHP Application Link](http://deploymentappphp-env.ees7a4yivx.us-east-1.elasticbeanstalk.com/)

## Steps on cretaing deployment environment:

### Elastic beanstalk
- Open the AWS Elastic beanstalk console.
- Select get started or Create new Application.
- Give your app a name, choose region, select platform (PHP), select sample application and click create.

### Code pipeline
- On your AWS CodePipeline console click create pipeline.
![Screen Screen](https://raw.githubusercontent.com/sadhikari07/deployment-app-php/master/assets/ScreenOne.png) 
- Choose a pipeline name, select new service role and click next.
![Screen Screen](https://raw.githubusercontent.com/sadhikari07/deployment-app-php/master/assets/ScreenTwo.png)
- Choose source provider (gitHub) and connect to gitHub by providing your credentials.
![Screen Screen](https://raw.githubusercontent.com/sadhikari07/deployment-app-php/master/assets/ScreenThree.png)
- Choose the repository and the branch (master) that you want to deploy.
- Select use GitHub webhooks and click next.
![Screen Screen](https://raw.githubusercontent.com/sadhikari07/deployment-app-php/master/assets/ScreenFour.png)
- Select skip build stage and click next.
![Screen Screen](https://raw.githubusercontent.com/sadhikari07/deployment-app-php/master/assets/ScreenFive.png)
- Choose deploy provider (Elastic Beanstalk), and choose the region, application name, and environment name(should auto-populate), and click next.
![Screen Screen](https://raw.githubusercontent.com/sadhikari07/deployment-app-php/master/assets/ScreenSix.png)
- Click create pipeline.
![Screen Screen](https://raw.githubusercontent.com/sadhikari07/deployment-app-php/master/assets/ScreenEight.png)



- To see auto-update, edit the index.php file and merge the commit to master. You should see the updates on your deployed website.

## Screenshots of pipeline updating after change in the master of the repo and once update is complete: 

![Screen Screen](https://raw.githubusercontent.com/sadhikari07/deployment-app-php/master/assets/screen15.png)
![Screen Screen](https://raw.githubusercontent.com/sadhikari07/deployment-app-php/master/assets/screen16.png)


# Adding a Build stage 
![alt_text](https://github.com/river-ceanne/deployment-app-php/blob/master/assets/Screen%20Shot%202019-07-17%20at%2011.36.46%20AM.png)
![alt_text](https://github.com/river-ceanne/deployment-app-php/blob/master/assets/Screen%20Shot%202019-07-17%20at%2011.37.25%20AM.png)
![alt_text](https://github.com/river-ceanne/deployment-app-php/blob/master/assets/Screen%20Shot%202019-07-17%20at%2011.37.34%20AM.png)
![alt_text](https://github.com/river-ceanne/deployment-app-php/blob/master/assets/Screen%20Shot%202019-07-17%20at%2011.38.04%20AM.png)
![alt_text](https://github.com/river-ceanne/deployment-app-php/blob/master/assets/Screen%20Shot%202019-07-17%20at%2011.40.39%20AM.png)
![alt_text](https://github.com/river-ceanne/deployment-app-php/blob/master/assets/Screen%20Shot%202019-07-17%20at%2011.42.34%20AM.png)

 


## Itegration 
- This app requires a running `Apache` or `nginx` server pointed to the folder where index.php resides

## Testing
- Open a terminal and change to the folder containing this application
- Run the tests
  - `./vendor/bin/phpunit --bootstrap vendor/autoload.php index.test.php`
  
  
 ## Reference: 
 https://aws.amazon.com/getting-started/tutorials/continuous-deployment-pipeline/
