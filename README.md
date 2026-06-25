# Custom ESXi 8 ISO with Network Drivers

This repository contains a PowerCLI workflow for building a custom VMware ESXi 8 ISO image with additional community network drivers.

## Purpose

Some lab servers and small business machines use network adapters that are not supported by the default ESXi installer. This script shows how to create a custom ESXi installation ISO that includes the required network driver package.

## Use Case

- Homelab ESXi installation
- Small virtualization servers
- Hardware with unsupported network adapters
- Infrastructure troubleshooting and deployment preparation

## Requirements

- VMware PowerCLI
- ESXi offline depot ZIP file
- Community network driver offline bundle
- Windows or PowerShell environment with required permissions

## Workflow

The script performs these steps:

1. Add the ESXi software depot
2. Add the network driver software depot
3. Clone the default ESXi image profile
4. Add the community network driver package
5. Export the new image profile as an ISO file

## Notes

Update file paths before running the script. The original script uses local paths under `c:\tmp`.

## Portfolio Value

This repository is useful for showing infrastructure and virtualization experience. It is not a primary freelance portfolio project, but it supports an infrastructure/backend profile.

## Recommendation

Keep this repository public only if you want to show VMware and infrastructure experience. Otherwise, archive or make it private.

## Author

Mahdi Aghtaee
