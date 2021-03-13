# amazon-managed-workflows-for-apache-airflow-playground

learn [Amazon Managed Workflows for Apache Airflow](https://docs.aws.amazon.com/mwaa/index.html)

## Install Steps

1. create S3 bucket with versioning enabled
2. create VPC - this is where RDS Postgres for airflow data lives, the airflow web UI runs in a container here
3. create aiflow environment

## Notes

* you create named MWAA environments and they each have own configuration
* airflow ui exposed publically or private within VPC
* login to [airflow ui with IAM user](https://docs.aws.amazon.com/mwaa/latest/userguide/access-airflow-ui.html)
* can create [web login token](https://docs.aws.amazon.com/mwaa/latest/userguide/access-airflow-ui.html#call-mwaa-apis-web) via AWS CLI
* upload DAG .py files to `dag` path in S3
* run DAGs via airflow cli
* invoke [DAG via lambda](https://docs.aws.amazon.com/mwaa/latest/userguide/samples-lambda.html)
* install additional deps by providing requirements.txt
* auto scales up and down via Apache Celery Executor by adding / removing worker containers as needed

## Resources

* [Amazon Managed Workflows for Apache Airflow](https://docs.aws.amazon.com/mwaa/index.html)
* [Interacting with Amazon Managed Workflows for Apache Airflow via the command line](https://dev.to/aws/interacting-with-amazon-managed-workflows-for-apache-airflow-via-the-command-line-4e91)
* [AWS CLI Command Reference | mwaa](https://awscli.amazonaws.com/v2/documentation/api/latest/reference/mwaa/index.html)
