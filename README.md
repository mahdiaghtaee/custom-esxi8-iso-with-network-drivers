###########################################################################
# Author: Mahdi Aghtaee
# Version: 1.0
##########################################################################

Add-EsxSoftwareDepot c:\tmp\ESXi-8.0b-21203435-standard.zip
Add-EsxSoftwareDepot c:\tmp\Net-Community-Driver_1.2.7.0-1vmw.700.1.0.15843807_19480755.zip

# Create new, custom profile
New-EsxImageProfile -CloneProfile "ESXi-8.0b-21203435-standard" -name "ESXi-8.0b-21203435-standard-Net-Drivers" -Vendor "sabasoft.org"

# Add community network driver package to custom profile
Add-EsxSoftwarePackage -ImageProfile "ESXi-8.0b-21203435-standard-Net-Drivers" -SoftwarePackage "net-community"

##############################################################################
# Export the custom profile to ISO
##############################################################################
Export-ESXImageProfile -ImageProfile "ESXi-8.0b-21203435-standard-Net-Drivers" -ExportToIso -filepath ESXi-8.0b-21203435-standard-Net-Drivers.iso

