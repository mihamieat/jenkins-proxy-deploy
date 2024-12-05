# HackaJenkins

## Instructions

### Export AWS Keys 🔑

- AWS Keys are essential for AWS EC2 intance deployment.

```sh
export AWS_ACCESS_KEY_ID=XXXX
export AWS_SECRET_ACCESS_KEY=XXXX
```

### Apply Terraform EC2 Deployment ↗️

- To deploy the Jenkins EC2 VM with Terraform do

```sh
terraform init
terraform apply
```

- Check that the instance has successfully been deployed.

```sh
aws ec2 describe-instances --instance-ids <instance-id>
```

### Apply Ansible Jenkins and Nginx Deployment ↗️

```sh
ansible-playbook -i ./ansible/ec2-inventory.yml ./ansible/playbook.yml --private-key rev-proxy.pem
```

## Notes 📝

### Terraform EC2

- An existing security group `launch-wizard-1` will be assigned to the created EC2 instance
- An xisting key pair `rev-proxy` as well
- The instance will be linked to the `default` AWS `VPC`.
