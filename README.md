# MLflow-Basic-Demo


MLFLOW_TRACKING_URI=https://dagshub.com/Subash7Lingden/MLflow-Basic-Demo.mlflow \
MLFLOW_TRACKING_USERNAME=Subash7Lingden \
MLFLOW_TRACKING_PASSWORD=e47cb2181458071797d31f2e25e11e1defd6bd99 \
python script.py


~~~bash
set MLFLOW_TRACKING_URI=https://dagshub.com/Subash7Lingden/MLflow-Basic-Demo.mlflow 
set MLFLOW_TRACKING_USERNAME=Subash7Lingden 
set MLFLOW_TRACKING_PASSWORD=e47cb2181458071797d31f2e25e11e1defd6bd99
```



MLflow-Basic-Demo
For Dagshub:
MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/MLflow-Basic-Demo.mlflow
MLFLOW_TRACKING_USERNAME=entbappy
MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0
python script.py

export MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/MLflow-Basic-Demo.mlflow

export MLFLOW_TRACKING_USERNAME=entbappy 

export MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0


### MLflow on AWS
MLflow on AWS Setup:
Login to AWS console.
Create IAM user with AdministratorAccess
Export the credentials in your AWS CLI by running "aws configure"
Create a s3 bucket
Create EC2 machine (Ubuntu) & add Security groups 5000 port
Run the following command on EC2 machine

sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv

sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell


## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-test-23

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI=http://ec2-54-147-36-34.compute-1.amazonaws.com:5000/