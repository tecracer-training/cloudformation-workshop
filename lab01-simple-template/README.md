# Lab 1: Simple template

Create a S3 bucket with the help of CloudFormation.

## Overview
1. Create a CloudFormation template that will create a S3 bucket named cloudformation-workshop-$username. Replace $username with your username (e.g. myname).
1. Create a CloudFormation stack based on your template.

## Instructions

### Create a template
1. Open ``lab01-stub.template`` with an editor of your choice. The stub file contains a skeleton to start from.
1. Add an ``AWSTemplateFormatVersion`` definition to your template (see [Template anatomy](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)).
1. Add a ``Description`` to your template (see [Template anatomy](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)).
1. Add a ``Resources`` section to your template (see [Template anatomy](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)).
1. Add a **S3 bucket** to the ``Resources`` section of your template (see [Resource Type: S3 bucket](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)).
1. Add ``BucketName`` as the only property to the ``Properties`` section of the S3 bucket. Be careful: bucket name has to be globally unique. Try ``cf-workshop-$username`` replace ``$username`` with your username.

### Create a stack based on the template
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose the template file you created for this lab.
1. Click **Next** button.
1. Insert ``lab01-$username`` as stack name. Replace ``$username`` with your username (e.g. lab01-myname).
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Review your input and click **Create** button.
1. Wait until your stack reaches status **CREATE_COMPLETE**.

### Test
locate your bucket in AWS Management Console 
OR
create a Index.html-File and upload it to the bucket (set permissions on file and bucket, change setting for static webserver)

### Delete your stack
1. Select your stack by clicking on row of the table.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Congratulations! You are done with the lab!

## Documentation
* [Template anatomy](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)
* [Resource Type: S3 bucket](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)

## Sample solution
This lab includes a sample solution ``lab01-sample-solution.template``. Use it if you are stuck during the creation of your template of if you want to review your results.