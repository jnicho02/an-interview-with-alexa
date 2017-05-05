https://sbstjn.com/serverless-alexa-skill-for-amazon-echo-with-aws-lambda.html

Servless the

$ npm install -g serverless
$ mkdir serverless-alexa-skill && cd serverless-alexa-skill
$ serverless create --template aws-python

Serverless: Generating boilerplate...
 _______                             __
|   _   .-----.----.--.--.-----.----|  .-----.-----.-----.
|   |___|  -__|   _|  |  |  -__|   _|  |  -__|__ --|__ --|
|____   |_____|__|  \___/|_____|__| |__|_____|_____|_____|
|   |   |             The Serverless Application Framework
|       |                           serverless.com, v1.12.1
 -------'

Serverless: Successfully generated boilerplate for template: "aws-python"
Serverless: NOTE: Please update the "service" property in serverless.yml with your service name



service: greyhound-alexa-skill

provider:
  name: aws
  runtime: python2.7
  stage: dev
  region: eu-west-1

functions:
  hello:
    handler: handler.hello
    events:
      - alexaSkill

$ sls invoke local -f hello
$ sls deploy
$ sls invoke -f hello

$ sls info

Service Information
service: greyhound-alexa-skill
stage: dev
region: eu-west-1
api keys:
  None
endpoints:
  None
functions:
  hello: greyhound-alexa-skill-dev-hello

$ brew install awscli
$ aws sts get-caller-identity --output text --query 'Account'
918093719737

ARN = arn:aws:lambda:eu-west-1:918093719737:function:greyhound-alexa-skill-dev-hello

https://developer.amazon.com/edw/home.html#/
