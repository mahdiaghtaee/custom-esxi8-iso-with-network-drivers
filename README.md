# Custom ESXi 8 ISO with Network Drivers

A small PowerCLI workflow for building a custom VMware ESXi 8 installation image with additional community network drivers.

## Why

Some lab and small-server hardware uses network adapters that are not included in the default ESXi installer. This workflow adds the required offline driver bundle to an ESXi image profile and exports a new ISO.

## Requirements

- VMware PowerCLI
- ESXi offline depot ZIP
- compatible community network-driver offline bundle
- Windows or PowerShell environment with the required permissions

## Workflow

1. Add the ESXi software depot.
2. Add the network-driver software depot.
3. Clone the default ESXi image profile.
4. Add the community driver package.
5. Export the customized profile as an ISO.

## Notes

Update the local depot and output paths before running the script. The original example uses paths under `C:\tmp`.

Driver compatibility depends on the ESXi build and the community driver bundle you select. Review package compatibility before using the resulting image on a production host.

## Author

Mahdi Aghtaee
