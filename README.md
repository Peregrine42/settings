settings
========

To set up an ubuntu share:

Add the user to the vboxsf group:
```bash
usermod -a -G vboxsf <username>
```

Add the following line to /etc/rc.local:
```bash
mount.vboxsf -w -o fmode=0777,dmode=0777 <shared_folder_name> /path/to/mount/point
```
