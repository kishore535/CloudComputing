#Road Traffic Severity Prediction in AWS SageMaker

Predicting the severity of accident to determine traffic delays 
Using AWS services to build, train and deploy a machine learning model and expose the model via an endpoint
This tool will provide response based on a scale ranging from 1 - 4 to provide an indication of traffic jam delays
1 - low severity - least impact on traffic
4 - high severity - most impact on traffic
Application areas include - 
Helpful for emergency responders to identify response protocols
GPS based clients like Google Maps and WAZE can use this tool to alert riders for possible delays and proactively provide alternate routes[5]

#Design Implementation Overview

Amazon’s S3 bucket is used to store the dataset 
SageMaker uses this data to train the machine learning model
In the SageMaker, the Notebook Instance is specified with ml.t2.medium type which is an Machine Learning Instance by AWS offering 250 hours of free-tier deployment. 
Trained model is then deployed and exposed via an endpoint.
AWS Lambda is used to create serverless application for handling requests, responses and invoking trained model endpoint.
API Gateway service is used to expose the Lambda application to external clients
