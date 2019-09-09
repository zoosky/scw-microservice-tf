## Install scaleway-cli

```bash
yay -Ss scaleway-cli
```

## Project strudture

```bash
 devops@devops  Documents/scaleway  tree 
.
├── main.tf
├── README.md
├── terraform.scw.tfvars
├── terraform.tfstate
├── terraform.tfstate.backup
└── variables.tf

0 directories, 6 files
```

## How to run terraform code with -var-file option

```bash
[root@devops$] terraform apply  -var-file=terraform.scw.tfvars 
data.scaleway_image.debian_stretch: Refreshing state...

Apply complete! Resources: 0 added, 0 changed, 0 destroyed.

Outputs:

id = 9a53e825-19f9-4e1f-b841-dd921e4e1b39
```

## Create terraform.scw.tfvars

```
# General

scw_region            = "par1"
scw_token             = "..."
scw_organization      = "..."
operating_system      = "CentOS 7.6"
instance_type         = "DEV1-S"
cloudinit_script_name = "modules/k8s_master/conf/cloudinit.sh"
```