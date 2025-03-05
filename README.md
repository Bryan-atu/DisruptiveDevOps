# DisruptiveDevOps
ADR-001: Choosing Flask with AWS Elastic Beanstalk for Deployment
Context

We are building a web application that requires a lightweight, scalable, and easily deployable framework. Flask is a minimalistic Python framework, and AWS Elastic Beanstalk provides a managed deployment environment, reducing the operational overheads.

Decision

We have decided to use:
Flask as the web framework due to its simplicity and flexibility.
AWS Elastic Beanstalk for deployment to automate provisioning, scaling, and monitoring.
SQL as the database for its reliability and integration with AWS services.
Gunicorn as the WSGI server to serve the Flask application.

Rationale

Flask
  Lightweight and easy to learn.
  Provides flexibility for adding features as needed.
  Well-supported.

AWS Elastic Beanstalk
  Provides automated scaling and load balancing.
  Simplifies deployment and infrastructure management.
  Offers built-in monitoring via AWS CloudWatch.

SQL
  Managed database service with automated backups and scaling.

Gunicorn
  A production-ready WSGI server.
  Supports multiple worker processes for better performance.

Consequences

Positives
Faster deployment with managed services.
Reduced DevOps overhead with AWS-managed infrastructure.
Scalability via Elastic Beanstalk auto-scaling.
Improved developer experience with Dockerized local development.

Negatives
Higher AWS costs compared to self-managed EC2 instances.
Limited customisation in Elastic Beanstalk environments.
Requires learning AWS Beanstalk CLI and configuration management.
