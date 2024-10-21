# Remount on all hosts

```bash
ansible all -m shell -a "mount -o remount /mnt"
```
execute until all hosts are remounted

# Check if remounted
```bash
ansible all -m shell -a "df -h"
```