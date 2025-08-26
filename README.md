# eip-ec2-clousformation
```
git clone https://github.com/atulkamble/eip-ec2-cloudformation.git
cd eip-ec2-cloudformation
```

⸻

🔹 AWS CloudFormation CLI Commands

1. Validate a Template

aws cloudformation validate-template \
  --template-body file://template.yaml

Checks syntax and structure of your CloudFormation template.

⸻

2. Create a Stack

aws cloudformation create-stack \
  --stack-name MyStack \
  --template-body file://template.yaml \
  --parameters ParameterKey=InstanceType,ParameterValue=t2.micro \
  --capabilities CAPABILITY_NAMED_IAM

Creates a new stack with parameters and required capabilities.

⸻

3. Update a Stack

aws cloudformation update-stack \
  --stack-name MyStack \
  --template-body file://template.yaml \
  --parameters ParameterKey=InstanceType,ParameterValue=t3.micro \
  --capabilities CAPABILITY_NAMED_IAM

Updates an existing stack with new configuration.

⸻

4. Delete a Stack

aws cloudformation delete-stack \
  --stack-name MyStack

Deletes the stack and all associated resources.

⸻

5. List All Stacks

aws cloudformation list-stacks \
  --stack-status-filter CREATE_COMPLETE UPDATE_COMPLETE


⸻

6. Describe a Stack

aws cloudformation describe-stacks \
  --stack-name MyStack

Displays details of a stack including outputs.

⸻

7. List Stack Resources

aws cloudformation list-stack-resources \
  --stack-name MyStack


⸻

8. Describe Stack Events

aws cloudformation describe-stack-events \
  --stack-name MyStack

Useful for troubleshooting deployment issues.

⸻

9. Get Template from Stack

aws cloudformation get-template \
  --stack-name MyStack


⸻

10. Preview Changes (Change Set)

aws cloudformation create-change-set \
  --stack-name MyStack \
  --change-set-name MyChangeSet \
  --template-body file://template.yaml \
  --parameters ParameterKey=InstanceType,ParameterValue=t3.medium \
  --capabilities CAPABILITY_NAMED_IAM

aws cloudformation describe-change-set \
  --stack-name MyStack \
  --change-set-name MyChangeSet


⸻

11. Delete Change Set

aws cloudformation delete-change-set \
  --stack-name MyStack \
  --change-set-name MyChangeSet


⸻

12. Wait for Stack Completion

aws cloudformation wait stack-create-complete --stack-name MyStack
aws cloudformation wait stack-update-complete --stack-name MyStack
aws cloudformation wait stack-delete-complete --stack-name MyStack


⸻
