# Backup daemon

## Building:
```bash
mkdir build
cd ./build
cmake ..
make
cd ..
```

## Starting daemon:
```bash
cp ./backup-daemon.service /etc/systemd/system/
cp ./backup.ini /etc/
systemctl daemon-reload
systemctl start backup-daemon
systemctl enable backup-daemon
```

## Pausing or continuing daemon:
```bash
systemctl kill -s SIGTSTP backup-daemon
systemctl kill -s SIGCONT backup-daemon
```

## Terminating daemon:
```bash
systemctl stop backup-daemon
```

## Inspecting logs:
```bash
systemctl status backup-daemon 
```
