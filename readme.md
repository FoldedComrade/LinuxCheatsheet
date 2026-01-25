# Claim a USB port for flashing devices via browser
```sudo setfacl -m u:<USERNAME>:rw /dev/<device>```

To list devices (typically /dev/TTYACM# or TTYUSB#)
```ls /dev/tty*```

# Burn an ISO to a drive
## Mint GUI
Right click .iso > Make Bootable USB

https://linuxmint-installation-guide.readthedocs.io/en/latest/burn.html

## CLI
to list drives

```sudo fdisk -l``` 

To burn iso w/ status

```sudo dd if=<FILENAME>.iso of=/dev/<DRIVE> status=progress```

```sync```

# Integrate an AppImage
AppImages are standalone files that don't get "installed" but do need made executable and then managed a bit to appear in the app menu
## Mint GUI
* Navigate to file, go Properties>Permissions and tick "Allow executing file as program"
* Move file to /home/<USERNAME>/Applications (or wherever you want to store them)
* Right click start menu>Edit Menu, select desired folder and select "New Item"
* Set name to whatever you want
* Set command to /home/user/Applications/<your appimage>
*   Some things (raspberry pi imager) might need sudo in front of the command
* OK
