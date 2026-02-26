# Lab M4.08 - Deploy EC2 with Terraform

## Infrastructure Created
- 2 web servers in public subnets with Apache
- 2 app servers in private subnets
- Web security group (HTTP/HTTPS/SSH)
- App security group (8080 from web SG only)

## Deployment
\`\`\`bash
terraform init
terraform apply -var="vpc_id=vpc-xxx" -var="my_ip=x.x.x.x/32" ...
\`\`\`

## Security
- Web tier: public-facing, HTTP/HTTPS open
- App tier: only accessible from web tier on port 8080
- SSH restricted to operator IP
