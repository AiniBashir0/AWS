# AutoScaling Group
### Auto Scaling Group (ASG) = Collection of EC2 instances managed as a single logical unit.

#### It ensures:

- Right number of instances (scale in/out automatically).
- High availability (replaces unhealthy instances).
- Cost optimization (only run required capacity).
- ASG works with Launch Template/Configuration (defines instance type, AMI, key pair, etc.)

## Lab
- create a webserver > actions > create image and template > create image
- name and description

#### ASG
- create > name > create a launch template > name > myAMI > choose image to created > instance type > select existing security group (created during ELB) > create
- go to create image tab > choose template > instance type: t-3.micro > AZ: choose all > attach to existinng load balancer > choose target group > checkmark - turn on ELB healthcheck > desired capacity > create
- go to ELB > Resource map > 4 instances (bcz ASG doesn't count/manager instances you created before creating ASG)
- instances > 2 new created by ASG > delete the original 2 instances created for ELB > run the site and it's still running
- if you delete any new instance, it will be recreated immediately
