# Manage-Infrastructure-using-Terraform-and-Ansible
In this lab, I built and configured cloud infrastructure using Terraform and Ansible, demonstrating full-stack provisioning and automation. The setup involved provisioning a control node, managing multiple web servers, and deploying different content to each group of servers.

1.Provisioned a Control Node using Terraform and set it up as the Ansible controller.

2. Launched Four EC2 Managed Nodes (Web Servers) using customized Terraform scripts.

Each server was assigned a public IP.

The list of servers and their IPs was documented for reference and connection.

3. Configured SSH Access:

Copied the control node’s SSH key into the managed node provisioning repo.

Enabled passwordless SSH between control and managed nodes for Ansible communication.

4. Created an hosts.ini Inventory File:

Grouped the four servers into two Ansible groups:

[einstein]: first two servers

[Cloud]: remaining two servers

5. Wrote and Executed Group-Specific Playbooks:

Created install_Einstein.yaml to install and configure Apache on the [einstein] group.

Verified successful execution using ansible-playbook and captured output screenshots.

6. Deployed Group-Specific Content:

Created install_Cloud.yaml to deploy a custom Cloud Computing webpage from a GitHub repository to the [Cloud] group.

Verified that the correct page was deployed on both Cloud group servers.

7. Validation and Testing:

Ensured both groups had the correct software and content deployed.

Accessed public IPs in the browser and confirmed the correct webpage loaded for each group.

https://drive.google.com/drive/folders/1hhvJ6VziEaJnqu81AcTH6SsNLSIt97Cb?usp=drive_link
