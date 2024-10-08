<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.9.5 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 5.67.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 5.67.0 |
| <a name="provider_local"></a> [local](#provider\_local) | 2.5.2 |
| <a name="provider_tls"></a> [tls](#provider\_tls) | 4.0.6 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_instance.instance](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/instance) | resource |
| [aws_key_pair.key-pair](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/key_pair) | resource |
| [aws_network_interface.interface](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/network_interface) | resource |
| [local_file.ssh-key](https://registry.terraform.io/providers/hashicorp/local/latest/docs/resources/file) | resource |
| [tls_private_key.tls-private-key](https://registry.terraform.io/providers/hashicorp/tls/latest/docs/resources/private_key) | resource |
| [aws_iam_instance_profile.ssm_instance_profile](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/iam_instance_profile) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_ami_id"></a> [ami\_id](#input\_ami\_id) | AMI ID for the EC2 instance | `string` | `""` | no |
| <a name="input_create_key"></a> [create\_key](#input\_create\_key) | Whether to create a key pair or not | `bool` | `true` | no |
| <a name="input_has_public_ip"></a> [has\_public\_ip](#input\_has\_public\_ip) | Whether the instance has a public IP address | `string` | `false` | no |
| <a name="input_instance_type"></a> [instance\_type](#input\_instance\_type) | EC2 instance type | `string` | `"t2.micro"` | no |
| <a name="input_key_name"></a> [key\_name](#input\_key\_name) | Key pair name | `string` | `"key-pair"` | no |
| <a name="input_private_ips"></a> [private\_ips](#input\_private\_ips) | List of private IPs for this instance | `list(any)` | `[]` | no |
| <a name="input_security_groups"></a> [security\_groups](#input\_security\_groups) | List of security groups | `list(any)` | `[]` | no |
| <a name="input_server_count"></a> [server\_count](#input\_server\_count) | Number of nodes to be created | `number` | `0` | no |
| <a name="input_server_prefix"></a> [server\_prefix](#input\_server\_prefix) | Instance name prefix | `string` | `"ec2"` | no |
| <a name="input_ssh_enabled"></a> [ssh\_enabled](#input\_ssh\_enabled) | Whether SSH access to the instance is enabled or not | `bool` | `true` | no |
| <a name="input_subnet_id"></a> [subnet\_id](#input\_subnet\_id) | Associated subnet ID | `string` | `""` | no |
| <a name="input_tags"></a> [tags](#input\_tags) | Instance tags | `map(string)` | `{}` | no |
| <a name="input_user_data_file"></a> [user\_data\_file](#input\_user\_data\_file) | User data file path | `string` | `""` | no |
| <a name="input_vpc_id"></a> [vpc\_id](#input\_vpc\_id) | Associated VPC ID | `string` | `""` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_hostnames"></a> [hostnames](#output\_hostnames) | List of hostnames (one per instance) |
| <a name="output_identity_file"></a> [identity\_file](#output\_identity\_file) | n/a |
| <a name="output_instance_id"></a> [instance\_id](#output\_instance\_id) | ID of the created EC2 instance |
| <a name="output_private_ips"></a> [private\_ips](#output\_private\_ips) | List of private/internal IPs |
| <a name="output_private_key"></a> [private\_key](#output\_private\_key) | n/a |
| <a name="output_public_ip"></a> [public\_ip](#output\_public\_ip) | Public IP of the created EC2 instance |
<!-- END_TF_DOCS -->