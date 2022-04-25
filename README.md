# eks-aws-infra

Follow instructions here: https://aws-quickstart.github.io/quickstart-amazon-eks/

## Requirements

- AWS EKS stack
- VPC: should use a big enough vpc, because each pod uses an IP.  a /24 has 256 ips available. /18 is bigger
- Should allow for private and public subnets
    - worker nodes run on private subnets
    - ELBs run on public subnets
- Node groups
    - need to drain old nodes, terminate old CFN template
    - "Updating AMI" in CFN template causes ungraceful termination of applications.
- Fargate profile
- Create KMS key for secrets encryption
- integrate synk: https://github.com/aws-quickstart/quickstart-eks-snyk/
- determine monitoring strategy
    - newrelic
    - prometheus + grafana

