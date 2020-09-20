# dotnetcore-serverless
aspnet core, dotnetcore boilerplate sever less for aws, azure, google 
## CQRS pattern for api (api command controller, api query controller )
## aws
#### auto create and mapping controller/action become lambda function keep name
#### auto register routing become aws api gateway by name
#### auto create and mapping console become lambda function
#### may be auto create SQS, event trigger to call lambda function
#### aws cloud front CDN for html, js, css (Angular)
## database
#### create ec2 to install mysql, redis, mongodb or use rdbs, dnynamodb

## diagram (CQRS)
### Client side:
#### Commands:
client action do sth --> (ajax request) <-request, response-> aws API gateway --> aws lambda function  (save db, enqueue, set cache, do sth)
#### Queries:
client want data ---> (ajax request) <-request, response-> aws API gateway <-- aws lambda function (read db, get cache, do sth)

### Server side:

- lambda function 

- ec2 scheduler to trigger event or invoke lambda function

- queue, stack, pubsub use aws SQS or redis in ec2


