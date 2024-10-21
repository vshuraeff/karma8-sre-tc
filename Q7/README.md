# server2server копирование:

## scp
```bash
scp -r -3 -i ~/.ssh/id_ed25519 user@server1:/var/lib/data user@server2:/var/lib/data
```

## rsync
```bash
ssh-add ~/.ssh/id_ed25519 && rsync -avz -e "ssh -A" user@server1:/var/lib/data user@server2:/var/lib/data
```