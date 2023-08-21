# AWS HA WebApp

## Deploy in AWS Console

### Deployment Sequence
1. network_infra.yml
2. server_deployment.yml
3. pipeline.yml

### Steps
1. Log in to the AWS console and navigate to CloudFormation.
2. Create a stack with new resources.
3. Upload the `.yml` file.
4. Fill in the parameters. References are provided in the `params` folder.
5. Submit the stack.

## Test it out

### CI/CD
1. Go to CodeCommit in the AWS console.
2. Clone the repository.
3. Copy the file from `demo-repo` into the cloned folder.
4. Commit and push the changes.
5. In AWS CodePipeline, approve the changes.
6. Access the page using HTTP. You should see the demo CodeDeploy page.

### HA
1. Go to EC2.
2. Terminate one of the virtual machines (VMs) created by the Auto Scaling Group.
3. Access the page. There should be no service interruption.
4. Go back to the EC2 instance page.
5. You should see that a new instance has been created by the Auto Scaling Group to ensure that two instances are running.
