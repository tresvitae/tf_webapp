#

## Additional EBS Volume check
```bash
sudo -s
df -h

mkfs.ext4 /dev/xvdh
mkdir data
mount /dev/xvdh data
df -h

vim /etc/fstab
/dev/xvdh /data ext4 defaults 0 0

df -h
umount data
mount data
```