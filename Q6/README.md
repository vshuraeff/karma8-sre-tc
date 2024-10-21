1.

```bash
    mdadm /dev/md0 --fail /dev/sdd1 --remove /dev/sdd1
    mdadm /dev/md1 --fail /dev/sdd2 --remove /dev/sdd2
    mdadm /dev/md2 --fail /dev/sdd3 --remove /dev/sdd3
```

2.
    
```bash
    sfdisk -d /dev/sda | sfdisk /dev/sdd
```

3.

```bash
    mkfs.xfs /dev/sdd4
```

4. 

```bash
    mdadm /dev/md0 --add /dev/sdd1
    mdadm /dev/md1 --add /dev/sdd2
    mdadm /dev/md2 --add /dev/sdd3
```

5. 

```bash
    mount /dev/sdd4 /mnt/sdd4
```

6. проверяем

```sh
    mdadm --detail /dev/md0
    mdadm --detail /dev/md1
    mdadm --detail /dev/md2
```

