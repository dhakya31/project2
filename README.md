# project2

1. Create Security Groups for 
    1. backend 
        with
        * 
2. Create RDS(mysql8)
    for that create
    1. subnet group
    2. parameter group
Note: Aurora vesion for BD is serverless fast and cheap in cost
        mysql
            user:admin
            pass:e4boht0IS5TFRu5GZ2ml
            endpoint:mysql.cphahtcix37d.ap-south-1.rds.amazonaws.com
3. Create memcached(1.6)
    for that create
    1. subnet group
    2. parameter group
        endpoint:cache-cluster.hbehgi.cfg.aps1.cache.amazonaws.com
4. Create active mq broker
    user:rabbit
    pass:jimmy@123456789
    endpoint:b-16ace2a6-938d-4282-bea5-807b58305ea3.mq.ap-south-1.amazonaws.com
* Add mysql SG id in project2-backend SG 
5. Create ec2 and intialize the rds
    run :apt install mysql-client
        :mysql -h rds endpoint -u admin -ppassword accounts
        :show tables;
        :exit
        :git clone url
        :mysql -h mysql.cphahtcix37d.ap-south-1.rds.amazonaws.com -u admin -pe4boht0IS5TFRu5GZ2ml accounts < src/main/resources/db_backup.sql
        :mysql -h mysql.cphahtcix37d.ap-south-1.rds.amazonaws.com -u admin -pe4boht0IS5TFRu5GZ2ml accounts
        :show tables;
6.  Create elastic beanstalk
7. Update SG and ELB
    * Enable Acls in elastic bean s3 bucket
    * edit heathcheck to /login and add listner https
    * Edit project2-backend sg allow ports 3306, 11211, 5672 from bean app sg
8. Build and Deploy artifact
    * Update the url of mysql, rabbitmq, and memcache(port also) in application.properties file
    * Build artifact locally
    * Go to bean stalk environment upload war file and deploy
    