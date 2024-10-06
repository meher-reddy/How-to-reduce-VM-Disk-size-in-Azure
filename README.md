# How-to-resize-VM-Disk-in-Azure
credits: https://jrudlin.github.io/2019-08-27-shrink-azure-vm-osdisk/

Objective: Reduce the Disk Size of Windows VM in Azure.
Procedure:
1. Connect to the VM that you want to perform the changes to.
2. Open "Create and format hard disk partitions" after booting into Windows.
3. Shrink the C:\ Drive to your required storage level.
4. Shut down the VM.
5. Download the [script](https://github.com/jrudlin/Azure/blob/master/General/Shrink-AzDisk.ps1) and update fields 2, 3, 4, and 5.
6. Note for $DiskID, go to the disk that you want to resize, go to properties, copy the entire resource ID, and paste for $DiskID field.
7. now open the cloud shell in PowerShell and upload the updated Powershell script to the cloud shell.
8. Run the script by using ./script_name.ps1.
9. The script will take 10-15 min to complete the changes.
10. Verify the changes by going to the Disks page.
