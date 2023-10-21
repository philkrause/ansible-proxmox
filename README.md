# Proxmox Ansible Playbook

## Overview

This Ansible playbook is designed to interact with the Proxmox Virtual Environment (Proxmox VE) API. It provides an efficient way to create and delete identical virtual machines based on predefined VM Config.

## Prerequisites

Before using this playbook, make sure you have the following prerequisites:

- Proxmox VE server installed and accessible.
- You must create an API Token in Proxmox to use this tool. You will need the token, token name, and user, along with other variables for connecting to proxmox`

## Playbooks

### test.yml

This playbook tests the connection to the Proxmox API and verifies authentication.

Usage:

### create.yml

This playbook creates virtual machines based on the configuration in `vars.yml`. It uses predefined VM IDs and VM names to create VMs.

Usage:

### delete.yml

This playbook deletes virtual machines based on the VM IDs specified in `vars.yml`.

Usage:


## Configuration

Before running the playbooks, ensure you have configured the following variables in the `vars.yml` file:

- `PVE_IP`: The IP address or hostname of your Proxmox VE server.
- `PVE_API_USER`: Your Proxmox API user.
- `PVE_TOKEN_NAME`: The token name associated with your API user.
- `PVE_TOKEN`: Your Proxmox API token.
- `VM_IDS`: A list of VM IDs.
- `VM_NAMES`: A list of VM names.
- `ISO_URL`: The URL or path to the ISO file for VM installations.
- `VM_MEMORY`: The size of VM memory in MB.
- `VM_SOCKETS`: The number of CPU sockets for VM.
- `VM_CORES`: The number of CPU cores for VM.
- `VM_DISK_SIZE`: The size of the VM disk in GB.
- `VM_DISK_NAME`: The name of the VM disk.

**Note:** It's important to ensure that `VM_IDS` and `VM_NAMES` have the same length, where each ID corresponds to a name (e.g., VM_ID at index 0 corresponds to VM_NAME at index 0).

## Execution

1. Clone this repository to your local machine.

2. Configure the `vars.yml` file with your Proxmox server details, authentication, VM IDs, VM names, and additional parameters.

3. Run the playbooks using the `ansible-playbook` command, as shown in the Playbooks section.

## Troubleshooting

If you encounter issues or errors, refer to the "Troubleshooting" section in this README for common problems and solutions.

## License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to customize this README template to fit your specific project requirements. Include any additional information, dependencies, or troubleshooting steps that may be relevant to your users.
