# amazon-managed-workflows-for-apache-airflow-playground

learn [Amazon Managed Workflows for Apache Airflow](https://docs.aws.amazon.com/mwaa/index.html)

## Install Steps

1. create S3 bucket with versioning enabled
2. create VPC - this is where RDS Postgres for airflow data lives, the airflow web UI runs in a container here
3. create aiflow environment

## Notes

* airflow ui exposed publically or private within VPC
* login to [airflow ui with IAM user](https://docs.aws.amazon.com/mwaa/latest/userguide/access-airflow-ui.html)
* upload DAG .py files to `dag` path in S3
* invoke [DAG via lambda](https://docs.aws.amazon.com/mwaa/latest/userguide/samples-lambda.html)
* install additional deps by providing requirements.txt
* auto scales up and down via Apache Celery Executor by adding / removing worker containers as needed

## Resources

* [Amazon Managed Workflows for Apache Airflow](https://docs.aws.amazon.com/mwaa/index.html)
