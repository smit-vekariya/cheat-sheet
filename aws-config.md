# Revision Questions (AWS)
AWS, which stands for Amazon Web Services, is a cloud service provider that helps in providing the services of various fields of domains through the internet with the principle of “Pay as you use”. AWS was started in 2006 with 3 types of services such as storage, computing, and messaging. After, it enhanced its network by providing all the required services based on the market trends.

> 1.  What Is AWS And Why Is It So Popular?

Amazon Web Services (AWS), is an important cloud computing platform known for its wide service offerings. Its popularity is developed through its scalability, cost-effectiveness, and global infrastructure. Businesses increased the AWS to efficiently scale operations, reduce costs, and innovate rapidly.

> 2.  Explain The Key Components Of AWS.

AWS provides the fundamental components crucial for cloud computing such as EC2 provides scalable computing capabilities, S3 offers storage for all kinds of files, RDS manages many kinds of databases, and IAM ensures secured access through addressing Authentication and Authorization. These components collectively empower the users to create and deploy various applications seamlessly.

> 3.  What Is An EC2 Instance And How Does It Work?

Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is a virtual server in the cloud. When we launch this, it will run the selected operating system with a specified application stack. For instance, you can deploy a web server or a database in this EC2 service. It can also be configured for specific computing needs, making it a flexible and scalable solution.

> 4. Describe The Difference Between S3 And EBS In AWS.

S3 ( Simple Storage Service ) is an object storage service suitable for storing various data types of files that can accessed through the internet. In contrast, EBS ( Elastic Block storage ) is a block-level storage attached to EC2 instances, offering persistent and high-performance storage for applications like databases. EBS provides the raw storage hardware helpful for I/O operations where as S3 comes with pre configured file system. For understaning think of S3 as a file storage system and EBS as a hard drive.

> 5. How Does Auto Scaling Work In AWS? 

Auto Scaling is an aws service that provides dynamically adjusts, on running the number of EC2 instances based on traffic demand. For instance, during the high traffic periods, Auto Scaling adds instances , improving optimal performance as per the policies configuration. Conversely, while during low traffic, it will reduce the number of instances , optimizes the cost efficiency maintaining high availability.

> 6. How Is Data Transfer Handled In AWS?

The data transfer in AWS happens in between regions, within regions, and between the services. It is essential to consider that these data transfer comes with costs when designing the architectures. For example, transfer of the data between an EC2 instance and an S3 bucket within the same region is often free, but the transfer of data in between inter-region comes with charges.

> 7. What Is Amazon RDS, And What Database Engines Does It Support?

Amazon RDS ( Relational Database system) is a managed relational database service that deals with essential hardware infrastructure of Amazon. It supports for the various database engines such as MySQL, SQL Server, Oracle, PostgreSQL and MariaDB. RDS involves in simplifying the database administration tasks on inclusion of backups, software patching, and scaling. It helps the developers to focus on logic of the application rather than focusing on infrastructure setup and management.

> 8. What Is AWS Elastic Beanstalk, And How Does It Simplify Application Deployment?

https://www.w3schools.com/django/django_deploy_provider.php

AWS Elastic Beanstalk is a AWS managed service helps in providing simplifyed application’s deployment and management through automatically handling the infrastructure provision. It allows the developers to focus completely on writing the code. For example, you only need to upload your code for deploying web application , Elastic Beanstalk will care of the rest of underlying infrastructures provisioning of EC2 instances and load balancing.

> 9. What Is Amazon VPC And How Does It Help In Securing Your Resources?

https://aws.amazon.com/vpc/ \
https://aws.amazon.com/vpc/features/

Amazon VPC ( Virutal Private Cloud ) is an AWS service that helps the users to create isolated networks within AWS account through customizing IP address ranges and the defining their subnets. It helps in enhancing the security through controlling both the inbound and outbound of the traffic. For example, To host the web servers in public subnets and connecting to the databases placing in private subnets can be on configuring the VPC. It provides an additional layer of network security to the applications.

> 10. Describe The Use Of Amazon Route 53.

https://avinetworks.com/glossary/aws-route-53/

AWS Route 53 is a scalable and highly available Domain Name System (DNS) web service. It plays a crucial role in DevOps by managing domain names, routing traffic to resources like EC2 instances, load balancers, and providing health checks to ensure high availability

> 11. EC2 vs Elastic beanstalk

https://www.sitepoint.com/aws-elastic-beanstalk-vs-ec2/#:~:text=EC2%20(Elastic%20Compute%20Cloud)%20is,deployment%20and%20scaling%20of%20applications.

What are the key differences between AWS Elastic Beanstalk and EC2?

AWS Elastic Beanstalk and EC2 are both services provided by Amazon Web Services, but they serve different purposes. EC2 (Elastic Compute Cloud) is a service that provides scalable computing capacity in the AWS cloud. It is designed to make web-scale cloud computing easier for developers. On the other hand, Elastic Beanstalk is a Platform as a Service (PaaS) that simplifies the deployment and scaling of applications. It automatically handles the details of capacity provisioning, load balancing, scaling, and application health monitoring

When should I use AWS Elastic Beanstalk instead of EC2?

Elastic Beanstalk is ideal for developers who want to deploy and manage applications in the AWS Cloud but don’t want to worry about the infrastructure that runs those applications. It provides an environment to easily deploy and run applications in the language of your choice. If you want more control over the underlying infrastructure, EC2 would be a better choice.

> 12. What is EC2 in AWS, explain every thing that what is that and how its work with example of deploy in django.

EC2 stands for Elastic Compute Cloud. It's a web service offered by Amazon Web Services (AWS) that provides scalable, on-demand virtual computers (VMs) in the cloud. You can launch these VMs with various configurations of CPU, memory, storage, and operating system to run your applications.

```Key Benefits of EC2:```

1. Scalability: Easily scale your compute resources up or down to meet changing application demands. You only pay for what you use.
2. Elasticity: Provision and configure VMs in minutes, eliminating the need to manage physical servers.
3. Cost-Effectiveness: Pay-as-you-go model ensures you're not paying for idle resources.
4. Wide Range of Options: Choose from a vast selection of instance types optimized for different workloads, including compute-intensive, memory-intensive, and storage-intensive applications.
5. Security: Leverage industry-leading security features to protect your applications and data in the cloud.
6. Integration: EC2 integrates seamlessly with other AWS services like S3 storage, RDS databases, and VPC networking for a comprehensive cloud solution.

```How EC2 Works:```

1. Choose an Instance Type: Select an instance type that aligns with your application's resource requirements (CPU, memory, storage, etc.). EC2 offers a wide range of options to ensure a cost-effective fit.
2. Launch Your Instance: Use the AWS Management Console, AWS SDK, or command-line interface to launch an instance. This creates a virtual server in the cloud.
3. Configure Your Instance: Set up the operating system, install necessary software (like your Django framework), and configure your application to run on the instance.
4. Secure Your Instance: Implement security groups to control inbound and outbound network traffic.
5. Access Your Instance: Connect to your instance using SSH (for Linux) or Remote Desktop (for Windows) to manage your application.
6. Deploy Your Django Application: Transfer your Django project files to the instance, configure settings, and start your Django server.
7. Scale as Needed: As your application's traffic or requirements change, you can easily add or remove instances to scale your compute resources.

```Django Deployment Example:```

1. Create an EC2 Instance: Launch an instance with an appropriate Linux distribution (e.g., Ubuntu) and sufficient resources for your Django application.
2. Connect to the Instance: Use SSH to connect to your instance and establish a secure connection.
3. Install Dependencies: Use a package manager like apt-get or yum to install necessary software like Python, Django, and any other required libraries.
4. Transfer Your Django Project: Upload your Django application files to the instance using methods like scp or S3 file transfer.
5. Configure Django Settings: Edit your Django settings file (settings.py) to specify database connections, secret keys, and other application-specific parameters.
6. Set Up a Database (Optional): If your Django application needs a database, you can use a service like Amazon RDS (Relational Database Service) or configure a database server on your instance.
7. Collect Static Files: Run python manage.py collectstatic to gather static files (CSS, JavaScript, images) and place them in the appropriate Django static directory.
8. Run Migrations (Optional): If you're using a database, execute python manage.py makemigrations and python manage.py migrate to create and apply database schema changes.
9. Start the Django Development Server (Optional): For testing purposes, you can run python manage.py runserver 0.0.0.0:8000 (replace 8000 with your desired port) to start the Django development server. This makes your application accessible locally on the instance.
10. Configure a Web Server (Production): For production deployment, use a web server like Apache or Nginx to serve your Django application. Configure the web server to point to your Django application's WSGI file (typically wsgi.py).
11. Security Considerations: Implement security best practices like using HTTPS and access control mechanisms to protect your application from unauthorized access.

```Additional Considerations:```

1. Load Balancing: As you scale your deployment, consider using an AWS service like Elastic Load Balancing to distribute traffic across multiple EC2 instances for improved performance and redundancy.
2. Automatic Scaling: Leverage AWS Auto Scaling to automatically adjust the number of EC2 instances based on predefined metrics like CPU utilization, ensuring your application can handle traffic spikes.
3. Monitoring: Monitor your application's performance and resource

Ec2 instance upload on ubutu and connect with remote desktop(find better way to access all file of project in editor insted of access from shell. find in youtube): https://stackoverflow.com/questions/50100360/connecting-to-aws-ec2-instance-through-remote-desktop (you can use SSH find how to use SSH in youtube)

EC2 instace upload on window and connect with remote desktop: https://www.google.com/search?q=how+to+connect+remote+desktop+in+aws+ec2+instance&rlz=1C1ONGR_enIN1084IN1084&oq=how+to+connect+remote+desktop+in+aws+ec2+insrtace&gs_lcrp=EgZjaHJvbWUqCQgBECEYChigATIGCAAQRRg5MgkIARAhGAoYoAEyCQgCECEYChigATIJCAMQIRgKGKAB0gEJMTI0NjJqMGo3qAIIsAIB&sourceid=chrome&ie=UTF-8#fpstate=ive&vld=cid:8087a636,vid:9ypkPfRQg2o,st:74
