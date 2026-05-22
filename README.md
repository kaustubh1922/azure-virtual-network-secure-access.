<img width="1907" height="1080" alt="image" src="https://github.com/user-attachments/assets/6da70f41-fde9-413a-bac4-99126166367a" /># azure-virtual-network-secure-access.
# Configuring Secure Access to Workloads with Azure Virtual Networking

## Project Overview
This project demonstrates the implementation and configuration of secure Azure virtual networking services. The goal was to establish a secure, isolated network environment for workloads, control inbound and outbound traffic, and ensure safe connectivity between resources.

## Architecture Diagram



## Key Features & Configurations Implemented

### 1. Virtual Network (VNet) & Subnet Creation
* **VNet Name:** App-Vnet
* **Address Space:** `10.0.0.0/16`
* **Subnets Configured:**
  * `[App-Vnet]` (e.g., WebSubnet - 10.0.1.0/24)
  * `[Hub-Vnet]` (e.g., DataSubnet - 10.0.2.0/24)

### 2. Network Security Groups (NSGs)
* Created and associated NSGs to restrict traffic to workloads.
* **Inbound Rules:** Configured rules to allow specific traffic (e.g., HTTP/HTTPS on port 80/443, SSH/RDP only from authorized IPs).
* **Outbound Rules:** Restricted internet access from backend subnets to prevent data exfiltration.

### 3. Secure Workload Access

* **Example:** Implemented **Azure Bastion** to securely connect to virtual machines over SSL without exposing public IP addresses.

## Skills Demonstrated
* Cloud Network Architecture Design
* Traffic Filtering & Network Security (NSGs & ASGs)
* Secure Remote Management
* Azure Resource Provisioning & Management

## How to Verify the Deployment
1. Log into the Azure Portal.
2. Navigate to the **Network Watcher** to view the topology.
3. Test connectivity between subnets to verify that the NSG rules successfully block or allow intended traffic.
