
# Welcome to your CDK Python project!

This is a blank project for CDK development with Python.

The `cdk.json` file tells the CDK Toolkit how to execute your app.

This project is set up like a standard Python project.  The initialization
process also creates a virtualenv within this project, stored under the `.venv`
directory.  To create the virtualenv it assumes that there is a `python3`
(or `python` for Windows) executable in your path with access to the `venv`
package. If for any reason the automatic creation of the virtualenv fails,
you can create the virtualenv manually.

To manually create a virtualenv on MacOS and Linux:

```
$ python3 -m venv .venv
```

After the init process completes and the virtualenv is created, you can use the following
step to activate your virtualenv.

```
$ source .venv/bin/activate
```

If you are a Windows platform, you would activate the virtualenv like this:

```
% .venv\Scripts\activate.bat
```

Once the virtualenv is activated, you can install the required dependencies.

```
$ pip install -r requirements.txt
```

At this point you can now synthesize the CloudFormation template for this code.

```
$ cdk synth
```

To add additional dependencies, for example other CDK libraries, just add
them to your `setup.py` file and rerun the `pip install -r requirements.txt`
command.

## Useful commands

 * `cdk ls`          list all stacks in the app
 * `cdk synth`       emits the synthesized CloudFormation template
 * `cdk deploy`      deploy this stack to your default AWS account/region
 * `cdk diff`        compare deployed stack with current state
 * `cdk docs`        open CDK documentation

Enjoy!



cdk init app --language python
pip install -r requirements.txt
Create app directory with dockerfile and main.py
cdk list: this will ouput the app
cdk synth: This command performs basic validation of your CDK code, runs your CDK app, and generates a CloudFormation template from your CDK stack.

cdk bootstrap aws://730335307143/eu-central-1

    Bootstrapping prepares your AWS environment by provisioning specific AWS resources in your environment that are used by the AWS CDK. These resources are commonly referred to as your bootstrap resources. They include the following:

    Amazon Simple Storage Service (Amazon S3) bucket – Used to store your CDK project files, such as AWS Lambda function code and assets.

    Amazon Elastic Container Registry (Amazon ECR) repository – Used primarily to store Docker images.

    AWS Identity and Access Management (IAM) roles – Configured to grant permissions needed by the AWS CDK to perform deployments. For more information about the IAM roles created during bootstrapping, see IAM roles created during bootstrapping.

Change Bucket Name in .env file

aws cloudformation describe-stacks --stack-name AwsCdkRagFargateStack --query "Stacks[0].Outputs[?OutputKey=='LoadBalancerDNS'].OutputValue" --output text

AwsCdk-RagFa-a1TpSwcX5iaS-653394042.eu-central-1.elb.amazonaws.com

curl -X POST -H "Content-Type: application/json" -d '{"question":"What is a transformer?"}' http://AwsCdk-RagFa-a1TpSwcX5iaS-653394042.eu-central-1.elb.amazonaws.com/query