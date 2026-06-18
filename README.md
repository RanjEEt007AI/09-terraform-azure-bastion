# Terraform Azure Bastion

This project demonstrates how to create an Azure Bastion Host using Terraform.

## 📌 Prerequisites

Before running this project, make sure you have:

- Azure Subscription
- Terraform installed
- Azure CLI installed
- Logged into Azure account

```bash
az login
```

## 📂 Project Structure

```text
.
├── provider.tf
├── main.tf
├── .gitignore
└── README.md
```

## 🚀 Resources Created

This Terraform project creates:

- Azure Resource Group
- Azure Virtual Network (VNet)
- Azure Bastion Subnet
- Azure Public IP
- Azure Bastion Host

## ⚙️ Terraform Configuration

Azure Bastion requires a dedicated subnet:

```text
AzureBastionSubnet
```

Subnet name must be exactly `AzureBastionSubnet`.

## 🛠️ Commands to Run

Initialize Terraform:

```bash
terraform init
```

Validate configuration:

```bash
terraform validate
```

Preview execution plan:

```bash
terraform plan
```

Create resources:

```bash
terraform apply -auto-approve
```

## 📤 Output

After successful deployment:

```bash
bastion_id = /subscriptions/xxxx/resourceGroups/bastion-rg/providers/Microsoft.Network/bastionHosts/demo-bastion
```

## 📖 Resources Used

- azurerm_resource_group
- azurerm_virtual_network
- azurerm_subnet
- azurerm_public_ip
- azurerm_bastion_host

## 📝 Notes

- Azure Bastion provides secure RDP and SSH connectivity.
- No public IP is required directly on VMs.
- Traffic remains within Azure network.

## 🛠️ Author

Ranjeet Kumar

GitHub: RanjEEt007AI
