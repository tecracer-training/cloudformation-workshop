# Lab 7: Nested stacks

Making use of nested stacks. Use modules trying to avoid complex and large templates.

## Overview
1. Create a CloudFormation template combining to other templates.
1. Create a CloudFormation stack based on your template.

## Instructions

### Create a template
1. Open ``lab07-stub.template`` with an editor of your choice. The stub file contains a skeleton to start from.
1. Add a resource to create a child stack based on ``https://s3-eu-west-1.amazonaws.com/courses.awsplayground.net/cloudformation-workshop/cflab07-ec2-stack.template`` (see [Resource Type: CloudFormation Stack](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html)).
1. Add a resource to create a child stack based on ``https://s3-eu-west-1.amazonaws.com/courses.awsplayground.net/cloudformation-workshop/cflab07-s3-stack.template`` (see [Resource Type: CloudFormation Stack](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html)).
1. Forward all parameters from parent template to ``sub-ec2-stack`` stack.
1. Add outputs referencing outputs from ``sub-ec2-stack`` stack (see [Resource Type: CloudFormation Stack](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html)).


### Create a stack based on the template
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose the template file you created for this lab.
1. Click **Next** button.
1. Insert ``lab07-$username`` as stack name. Replace ``$username`` with your username (e.g. lab07-myname).
1. Select a random subnet as parameter for **Subnet**.
1. Select the ``qwikLABS...`` key as parameter for **Key Pair**.
1. Insert ``http://www.tecracer.de/`` or a website you own for **URL**.
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Review your input and click **Create** button.
1. Wait until your stack reaches status **CREATE_COMPLETE**.

### Test
1. select your stack and click on **Outputs**. You should see the Instance Id and public IP address of the EC2 instance
1. Switch to S3 in the management console and look for the created bucket

### Delete your stack
1. Select your stack by clicking on row of the table.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Congratulations! You are done with the lab!

## Documentation
* [Resource Type: CloudFormation Stack](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html)

## Sample solution
This lab includes a sample solution ``lab07-sample-solution.template``. Use it if you are stuck during the creation of your template of if you want to review your results.