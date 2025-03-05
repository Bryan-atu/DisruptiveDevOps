# DisruptiveDevOps
ADR-001: Choosing Flask with AWS Elastic Beanstalk for Deployment
Context

We are building a web application that requires a lightweight, scalable, and easily deployable framework. <br />
Flask is a minimalistic Python framework, and AWS Elastic Beanstalk provides a managed deployment environment, reducing the operational overheads.<br />

Decision

We have decided to use: <br />
Flask as the web framework due to its simplicity and flexibility. <br />
AWS Elastic Beanstalk for deployment to automate provisioning, scaling, and monitoring. <br />
SQL as the database for its reliability and integration with AWS services. <br />
Gunicorn as the WSGI server to serve the Flask application.<br />

Rationale<br />
<hr>
Flask <br />
  Lightweight and easy to learn. <br />
  Provides flexibility for adding features as needed. <br />
  Well-supported.<br />

AWS Elastic Beanstalk <br /> 
  Provides automated scaling and load balancing.<br />
  Simplifies deployment and infrastructure management.<br />
  Offers built-in monitoring via AWS CloudWatch. <br />

SQL
  Managed database service with automated backups and scaling. <br />

Gunicorn
  A production-ready WSGI server.<br />
  Supports multiple worker processes for better performance. <br />
  
Consequences

Positives <br />
<hr>
Faster deployment with managed services. <br />
Reduced DevOps overhead with AWS-managed infrastructure. <br />
Scalability via Elastic Beanstalk auto-scaling. <br /> 
Improved developer experience with Dockerized local development.<br />

Negatives
<hr>
Higher AWS costs compared to self-managed EC2 instances. <br />
Limited customisation in Elastic Beanstalk environments. <br />
Requires learning AWS Beanstalk CLI and configuration management. <br />
