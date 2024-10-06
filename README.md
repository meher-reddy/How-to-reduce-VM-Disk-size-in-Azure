# How-to-resize-VM-Disk-in-Azure
credits: https://jrudlin.github.io/2019-08-27-shrink-azure-vm-osdisk/

Objective: Reduce the Disk Size of Windows VM in Azure.
Procedure:
1. Connect to the VM that you want to perform the changes to.
2. Open "Create and format hard disk partitions" after booting into Windows.
3. Shrink the C:\ Drive to your required storage level.
4. Shut down the VM.
5. Download the [script](https://github.com/jrudlin/Azure/blob/master/General/Shrink-AzDisk.ps1) and update fields 2, 3, 4, and 5.
6. For the Disk Size field enter the size that you wish to reduce the disk size to, eg: 22, 32, 30. (Must be greater than the C:\ drive size after shrinking).
7. Note for $DiskID, go to the disk that you want to resize, go to properties, copy the entire resource ID, and paste for $DiskID field.
8. now open the cloud shell in PowerShell and upload the updated Powershell script to the cloud shell.
9. Run the script by using ./script_name.ps1.
10. The script will take 10-15 min to complete the changes.
11. Verify the changes by going to the Disks page.
