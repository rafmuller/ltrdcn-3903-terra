# Terraform Section for LTRDCN-3903

This repository contains Terraform code to set up the necessary infrastructure for the LTRDCN-3903 project. Terraform is used to provision NXOS devices and configure them for a VXLAN/EVPN configuration.

## Prerequisites

- Ensure you have Terraform installed on your machine.
- You need access to the NXOS devices that will be configured.
- Make sure you have the necessary credentials and permissions to access the devices.
- The NXOS devices should be reachable from the machine where you run Terraform.

## About

This repository contains a single terraform module that was developed as an example for the LTRDCN-3903 project. The module is designed to be reusable and can be adapted for different environments.

The data directory contains the necessary data files for the module. These are structured in YAML format and utilize special utilities that Cisco has designed for merging many YAML files into a single in memory structure for use in the module.

## Usage

After you have installed Terraform and cloned this repository, you can use the following commands to set up the infrastructure:

1. Navigate to the directory containing the Terraform files:
   ```bash
   cd path/to/terraform/directory
   ```
2. Initialize Terraform:
   ```bash
   terraform init
   ```
3. Validate the Terraform configuration:
   ```bash
   terraform validate
   ```

You have to populate the YAML files in the example data directory with the necessary configuration data for your NXOS devices. Since this module is designed specifically to this LAB for Cisco Live, the data structure isn't documented. Functionality is limited to this specific use case, but can provide a good starting point for similar projects.

4. Apply the Terraform configuration:
   ```bash
   terraform apply
   ```

5. Follow the prompts to confirm the changes. Terraform will then provision the NXOS devices and apply the configurations defined in the YAML files.
6. Once the process is complete, you can verify the configurations on your NXOS devices.


