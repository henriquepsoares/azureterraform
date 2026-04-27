# ☁️ Terraform Azure Windows Server VM

🚀 This project uses **Terraform** with the **AzureRM provider** to provision a complete cloud infrastructure in Microsoft Azure, including networking, security, and a Windows Server virtual machine.

---

## 📦 Technologies Used

- 🧱 Terraform
- ☁️ Microsoft Azure (AzureRM Provider)
- 🌐 Virtual Network (VNet)
- 🔐 Network Security Group (NSG)
- 🖥️ Windows Virtual Machine

---

## 🏗️ What This Project Creates

This project automates the deployment of the following infrastructure:

---

### 🏢 Resource Group
- Creates a resource group named:
  - `rg-vmwindowsserver`

---

### 🌐 Virtual Network (VNet)
- Address spaces:
  - `10.0.0.0/16`
  - `192.168.0.0/16`

---

### 🔀 Subnet
- Subnet created inside the VNet:
  - `10.0.2.0/24`

---

### 🌍 Public IP
- Static public IP for external access
- DNS configured:
  - `vmwinservertf.eastus.cloudapp.azure.com`

---

### 🔌 Network Interface (NIC)
- Connects the VM to the network
- Includes both private and public IPs

---

### 🔐 Network Security Group (NSG)
- Controls inbound traffic to the VM

#### 📥 Automatically created rules:
| Port | Service |
|------|--------|
| 80   | HTTP 🌐 |
| 443  | HTTPS 🔒 |
| 3389 | RDP (Remote Desktop for Windows) 🖥️ |
| 22   | SSH 🔑 |

---

### 🖥️ Virtual Machine (Windows Server)
- Windows Server VM deployed in Azure
- Connected to the VNet and protected by NSG rules

---

## ⚙️ How to Use This Project

### 1️⃣ Initialize Terraform
```bash
terraform init
2️⃣ Validate configuration
terraform validate
3️⃣ Review execution plan
terraform plan
4️⃣ Deploy infrastructure
terraform apply
🧹 Destroy infrastructure
terraform destroy

⚠️ Important Notes

The default region used in this project is: eastus 🌎
Some VM SKUs may not be available depending on Azure capacity
If you encounter a SkuNotAvailable error, try:
Changing the region (e.g. westeurope)
Changing the VM size


🧠 What You Learn From This Project

This project demonstrates:

Infrastructure as Code (IaC) 🏗️
Cloud infrastructure automation ☁️
Virtual networking and segmentation 🔀
Security with NSG rules 🔐
Virtual machine deployment on Azure 🖥️
👨‍💻 Author

Professor Henrique Soares
Cloud & DevOps Infrastructure Project 🚀

⭐ If you like this project

Give it a ⭐ on GitHub and feel free to contribute or improve it!