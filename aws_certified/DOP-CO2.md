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
