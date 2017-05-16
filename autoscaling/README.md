# AutoScaling Cloudformation
You Can Create a AutoScaling group and Launch config for the given AMI using this template on AWS CloudFormation.

## Details
Cloud formation Template will launch minimum one instance and depending upon the load it will scale to the desired max count given.

Following will be created as part of the stack.
- LaunchConfig with the Given AMI ID
- AutoScaling Group
- Instance will be attached to the ELB Name given as a parmeter.
- Scaling Policies to Scale In and Scale Out based on CPU Threshold.
- A Custom parameter is given to help configure bash script as part of provisioning the instance launched through Autoscaling.
  This is given to ensure that there is no need to configure/update launch config every time if there is any changes.
  We can update the logic as required in the bash script passed as a parmeter to the stack and that will be executed as part of bootstrap.
