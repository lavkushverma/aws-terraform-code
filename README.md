# Terraform EC2 VPC Endpoint

This Terraform module creates an AWS EC2 VPC endpoint with an associated security group.

## Features

- ✅ Creates EC2 Interface VPC Endpoint
- ✅ Configurable security group with HTTPS access
- ✅ Support for private DNS
- ✅ Optional EC2 Messages endpoint for SSM
- ✅ Fully customizable with tags
- ✅ Multi-subnet support

## Prerequisites

- Terraform >= 1.0
- AWS Provider ~> 5.0
- Valid AWS credentials configured
- Existing VPC and subnets

## Usage

### Basic Example

```hcl
module "ec2_endpoint" {
  source = "./terraform-ec2-endpoint"

  project_name = "my-app"
  vpc_id       = "vpc-0123456789abcdef0"
  vpc_cidr     = "10.0.0.0/16"
  subnet_ids   = ["subnet-abc123", "subnet-def456"]

  tags = {
    Environment = "production"
    ManagedBy   = "terraform"
  }
}
```

### Complete Example with EC2 Messages

```hcl
module "ec2_endpoint" {
  source = "./terraform-ec2-endpoint"

  project_name                 = "my-app"
  vpc_id                       = "vpc-0123456789abcdef0"
  vpc_cidr                     = "10.0.0.0/16"
  subnet_ids                   = ["subnet-abc123", "subnet-def456"]
  private_dns_enabled          = true
  create_ec2messages_endpoint  = true

  tags = {
    Environment = "production"
    Team        = "platform"
    ManagedBy   = "terraform"
  }
}
```

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| project_name | Name of the project | `string` | `"my-project"` | no |
| vpc_id | ID of the VPC | `string` | n/a | yes |
| vpc_cidr | CIDR block of the VPC | `string` | n/a | yes |
| subnet_ids | List of subnet IDs | `list(string)` | n/a | yes |
| private_dns_enabled | Enable private DNS | `bool` | `true` | no |
| create_ec2messages_endpoint | Create EC2 Messages endpoint | `bool` | `false` | no |
| tags | Additional tags | `map(string)` | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| ec2_endpoint_id | ID of the EC2 VPC endpoint |
| ec2_endpoint_arn | ARN of the EC2 VPC endpoint |
| ec2_endpoint_dns_entries | DNS entries for the endpoint |
| ec2_endpoint_network_interface_ids | Network interface IDs |
| security_group_id | ID of the security group |
| ec2messages_endpoint_id | ID of EC2 Messages endpoint (if created) |

## Quick Start

1. **Clone the repository:**
   ```bash
   git clone 
   cd terraform-ec2-endpoint
   ```

2. **Copy the example variables:**
   ```bash
   cp terraform.tfvars.example terraform.tfvars
   ```

3. **Edit terraform.tfvars with your values:**
   ```bash
   vim terraform.tfvars
   ```

4. **Initialize Terraform:**
   ```bash
   terraform init
   ```

5. **Plan the deployment:**
   ```bash
   terraform plan
   ```

6. **Apply the configuration:**
   ```bash
   terraform apply
   ```

## What is an EC2 VPC Endpoint?

An EC2 VPC endpoint allows you to privately connect your VPC to AWS EC2 service without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect. This provides:

- **Enhanced Security**: Traffic stays within AWS network
- **Cost Savings**: No data transfer charges for VPC endpoint traffic
- **Better Performance**: Lower latency for EC2 API calls

## License

MIT License - feel free to use this in your projects!

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## Author

Created with ❤️ for the Terraform community
