# AWS SageMaker: Sign In, Set up SageMaker Studio and Use Jupyter Notebook Instance

Author: Mariana Alanis

Date: March, 2024

## Sign Up for AWS Account

First, head over to [AWS](https://aws.amazon.com/) and create an account. Note the following points:

- You have to provide your Credit Card Information.
- You might be charged depending on your usage.
- There is an option for a free tier, but it keeps changing.

Sign up for an [AWS Free Tier Account](https://aws.amazon.com/free/) [here](https://aws.amazon.com/free/).

Once you sign up for your AWS Account, you will see your Amazon Console Home.

## Create S3 Bucket for Storage

1. Search for S3 in the Search Bar.
2. Select "Create a bucket."
3. Give a name and select the below options.

Great, you have now successfully created your S3 bucket.

Keep the rest of the settings as default and create your S3 bucket!

## Create ECR (Elastic Container Registry)

1. Here, we will create a repository.
2. Select "Create a repository" and enter a unique name.
3. You can get your ARN by simply copying the URI below. You will need this to set up SageMaker in the next step.

## Set up SageMaker on AWS

1. Your Home Console will look something like this:

   ![Home Console](<link to image>)

2. Search for SageMaker in the search bar and select the first option.
3. Once you are on the Amazon SageMaker page, select "Getting Started" from the left pane.

### Create a Role

1. Select "Create a Role" and enter the information for your desired role.

### Configure ML Activities

1. Click Next and select all the options as mentioned below. Don’t select more than 10 roles — AWS does not allow it.
2. Add the bucket name you created in all of the configuration fields. First, enter S3 bucket name.
3. Next, enter the S3 bucket again and the URI that you copied. We have to convert the URI that we have into ARN format. Here is mine: `arn:aws:ecr:ap-southeast-2:038365619140:repository/mlopsanish`
4. Next, enter your S3 bucket again and primary for the default workgroup.
5. Click the next button.

### Add Additional Policies & Tags

### Review Role

### Validate

Search for IAM, and select Roles.

You will see your role show up here, with the prefix SageMaker.

## Create Jupyter Notebook Instance

### SageMaker Domain

1. Next, go back to SageMaker and configure a SageMaker Domain.
2. Do a quick setup.
3. It will work on creating a domain.
4. Once it is set, you will be able to access AWS SageMaker Studio.

### Create Jupyter Notebook Instance on AWS SageMaker

1. Search for SageMaker Studio in AWS Home Console.
2. Go to Notebook Instances on the left panel as shown.
3. Select "Create Notebook Instance."
4. Create a notebook instance and hit the orange "create."
5. You will see the notebook being created.
6. Once it is set up, you will see the Create Notebook instance being “InService.”
7. Select your notebook and then select Open JupyterLab.
8. Select “Open Jupyter” and Tada! In a few minutes, you will have Jupyter Notebook hosted on the cloud.
9. Select `conda3_python` as the interpreter of choice and run!

