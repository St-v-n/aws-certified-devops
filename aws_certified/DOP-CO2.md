# AWS Certified DOP-CO2

## Acture Exam Questions from examtopics

### Topic 1 - Exam A

#### Question #1
A company has a mobile application that makes HTTP API calls to an Appication Load Balancer(ALB).
The ALB routes requests to an AWS Lambda function.
Many different versions of the application are in use at any given time, including versions that are in testing by a subset of users.
The version of the application is defined in the user-agent header the is sent with all requests to the API.
After a series of recent changes to the API, the company has obseved issues with the application.
The company needs to gather a metric for each API operation by response code for each version of the appliaction that is is use.
A DevOps engineer has modified the Lambda function to extract the API operation name, version information from th user-agent header and response code.
Which additional set of actions should the DevOps engineer take to gather the required metrics?

A. Modify the Lambda function to write the API operation name, response code, and version number as a log line to an Amazon CloudWatch Logs log group.
    Configure a CloudWatch Logs metric filter that increments a metric for each API operation name.
    Specify response code and application version as dimensions for the metric.

B. Modify the Lambda function to write the API operation name, response code, and version number as a log line to an Amazon CloudWatch Logs log group.
    Configure a CloudWatch Logs Insights query to populate CloudWatch metrics from the log lines.
    Specify response code and application version as dimensions for the metric.

C. Configure the ALB access logs to write to an Amazon CloudWatch Logs log group. Modify the Lambda function to respond to the ALB with the API operation name, response code, and version number as response metadata.
    Configure a CloudWatch Logs metric filter that increments a metric for each API operation name.
    Specify response code and application version as dimensions for the metric.

D. Configure AWS X-Ray integration on the Lambda function. Modify the Lambda function to create an X-Ray subsegment with the API operation name, response code, and version number.
    Configure X-Ray insights to extract an aggregated metric for each API operation name and to publish the metric to Amazon CloudWatch.
    Specify response code and application version as dimensions for the metric.

#### Question #2
A company provides an application to customers.
The appliaction has an Amazon API Gateway REST API that invokes an AWS Lambda function.
On initialization, the Lambda function loads a large amount of data from an Amazon DynamoDB table. The data load process results in long cold-start times of 8-10 seconds.
The DynamoDB table has DynamoDB Accelerator(DAX) configured.
Customers report that the application intermittently takes a long time to respond to requests. The application receives thousands of requests throughout the day.
In the middle of the day, the application experiences 10 times more requests than at any other time of the day.
Near the end of the day, the application's request volume decreases to 10% of its normal total.
A DevOps engineer needs to reduce the latency of the Lambda function at all times of the day.
Which solution will meet these requirements?

A. Configure provisioned concurrency on the Lambda function with a concurrency value of 1. Delete the DAX cluster for the DynamoDB table.

B. Configure reserved concurrency on the Lambda function with a concurrency value of 0.

C. Configure provisioned concurrency on the Lambda function.
    Configure AWS Application Auto Scaling on the Lambda function with provisioned concurrency values set to a minimum of 1 and a maxaimum of 100

D. Configure reserved concurrency on the Lambda function.
    Configure AWS Application Auto Scaling on the API Gateway API with a reserved concurrency maximum value of 100.

#### Question #3
A company is adopting AWS CodeDeploy to automate its application deployments for a Java-Apache Tomcat application with an Apache Webserver.
The development team started with a proof of concept, created a deployment group for a devleoper environment, and performed functional tests within the application . After completion, the team will create additional deployment groups for staging and production.
The current log level is configured within the Apache settings, but the team wants to change this configuration dynamically when the deployment on the deployment group without having a differnt application revision for each group.
How can these requirements be met with the LEAST management overhead and without requiring different script versions for each deployment group?

A. Tag the Amazon EC2 instances depending on the deployment group. Then place a script into the application revision that calls the metadata service and the EC2 API to identify which deployment group the instance is part of. Use this information to configure the log level settings. Reference the script as part of the AfterInstall lifecycle hook in the appspec.yml file.

B. Create a script that uses the CodeDeploy environment variable DEPLOYMENT_GROUP_NAME to identify which deployment group the instance is part of. Use this information to configure the log level settings. Reference this script as part of the BeforeInstall lifecycle hook in the appspec.yml file.

C. Create a CodeDeploy custom environment variable for each environment. Then place a script into the application revision that checks this environment variable to identify which deployment group the instance is part of. Use this information to configure the log level settings. Reference this script as part of the ValidateService lifecycle hook in the appspec.yml fiel.

D. Create a script that uses the CodeDeploy environment variable DEPLOYMENT_GROUP_ID to identify which deployment group the instance is part of to configure the log level settings. Reference this script as part of the Install lifecycle hook in the appsepc.yml file. 