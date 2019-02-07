# The simplest way to create a RESTFUL API with Lambda and API Gateway
You can do this from macOS, Windows, or Cloud9 in AWS. 
Tested with Python 3.6.6 and pip 18.1 on macOS 10.14.2, using AWS us-east-1.
Make sure to create an account on aws.amazon.com.<br>
This walkthrough uses the <a  href="https://github.com/aws/chalice">Chalice Serverless Microframework</a>
to create a simple API with Python3 deployed to AWS API Gateway and Lambda.
<br>
No promises on Windows-based systems (sorry)!

Install and configure the AWS CLI<br>
<code>pip install awscli</code><br>
<code>aws configure</code>

Create a Python virtual environment<br>
<code>virtualenv -p python3 venv && source venv/bin/activate </code>

Install <a href="https://github.com/aws/chalice">Chalice</a><br>
<code>pip install chalice</code>

Create a new project<br>
<code>chalice new-project um-facts</code>

Deploy to AWS<br>
<code>cd um-facts && chalice deploy</code>

Test it out!<br>
<code>curl -X GET [your API URL]</code>

Adjust to taste and redeploy, possibly by <a href="https://github.com/dixonaws/restful_dynamo"> getting data from a DynamoDB table</a> or by
getting data from an <a href="https://github.com/dixonaws/restful_aurora">RDS database</a>.
You could also test locally with <code>chalice local</code>. 




