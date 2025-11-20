# Burn an ISO to a drive
## Mint GUI
Right click .iso > Make Bootable USB

https://linuxmint-installation-guide.readthedocs.io/en/latest/burn.html

## CLI
to list drives

```sudo fdisk -l``` 

o burn iso w/ status

```sudo dd if=<FILENAME>.iso of=/dev/<DRIVE> conv=fsync bs=4M status=progress```

```sync```
