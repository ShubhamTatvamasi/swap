# swap

create 100-GB swap file:
```bash
sudo fallocate -l 100G /swapfile
```

update permission to root only:
```bash
sudo chmod 600 /swapfile
```

mark file as swap file
```bash
sudo mkswap /swapfile
```

enable swapfile:
```bash
sudo swapon /swapfile
sudo swapon --show
```

check ram:
```bash
free -h
```

### swap off

comment `/swap.img` line and `reboot`
```bash
sudo swapoff -a
sudo vim /etc/fstab
```

