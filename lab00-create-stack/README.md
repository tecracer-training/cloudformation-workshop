# Lab 0: Create a CloudFormation stack

Create a CloudFormation stack based on an existing template.

## Overview
1. Create a CloudFormation stack based on an existing template.

## Instructions
### create a stack
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose file ``cloudformation-workshop/lab00-create-stack/demo-create-stack.template``.
1. Click **Next** button.
1. Insert ``lab00-$username``as stack name. Replace ``$username``with your username (e.g. lab00-myname).
1. Select a random subnet and the only available VPC as **Parameters**.
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Review your input and click **Create** button.
1. Wait until your stack reaches status **CREATE_COMPLETE**.

### Test
1. Select your stack by clicking on row of the table.
1. Switch to the **Outputs** tab.
1. Search for **HelloWorldURL* and click on the URL.
1. A website showing ``Hello World!`` should appear.

### delete your stack
1. Select your stack by clicking on row of the table again.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Congratulations! You are done with the lab!