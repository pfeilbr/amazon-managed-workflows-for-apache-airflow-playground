# amazon-managed-workflows-for-apache-airflow-playground

## Steps

1. create S3 bucket with versioning enabled
2. create VPC
3. create aiflow environment

* upload DAG .py files to `dag` path in S3
* invoke [DAG via lambda](https://docs.aws.amazon.com/mwaa/latest/userguide/samples-lambda.html)
* install additional deps by providing requirements.txt
* auto scales
