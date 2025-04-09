# Introduction 
Optimizing resources and reducing operational costs remain paramount goals for organizations of all sizes. One particularly effective strategy to achieve this is the automation of EC2 instance start and stop schedules. Imagine a scenario where your Amazon Web Services (AWS) EC2 instances automatically power down during off-hours, weekends, or holidays, only to spring back to life exactly when you need them. This level of precision and efficiency isn’t a futuristic dream but a practical reality that can significantly impact your bottom line. 
# step-by-step guide
Follow these steps to schedule your EC2-innstances for off hours:

1. Launching EC2 Instances:
   Let’s first start by creating 4 instances in our AWS account. We will have an 'env' tag, where 2 of the instances will have a value of 'dev' for the 'env' tag, 
   and the other 2 will have the value 'test' for the 'env' tag. We will be using the tag later in this blog as we run Lambda functions based on tags.

    ○  Create 2 EC2 instances, adding a tag key ‘env’ with the value ‘dev’.

    ○ Create another pair of instances with tag key ‘env’ and value ‘test'.

    ○ Now we have a total of 4 running instances.

2. Creating a Role:
   Create an IAM role with the necessary permissions for Lambda to manage EC2 instances.

3. Creating a Lambda Function:
   Create a Lambda function using the provided code.
   Configure the function with the appropriate IAM role.
   Test the function to ensure it can start and stop instances based on tags.
   Scheduling the Lambda Function

4. Set up CloudWatch Events Rules to schedule the Lambda function executions.
   
5. Define the schedule based on your requirements, specifying when to start and stop instances.
   
6. Using IaC (terraform) to deploy the infrastructure.
   # Reference:
   Kevin Kiruri
