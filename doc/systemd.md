basically `/podi start` is to be called some way or another

## systemd example

Many servers use systemd, so you can modify the text below and put it into `/etc/systemd/system/your-container.service`:

```
[Unit]
Description=your-container 
Wants=network-online.target
After=network-online.target

[Service]
Type=oneshot
User=username
Group=username
RemainAfterExit=yes
WorkingDirectory=/home/username/repository
ExecStart=/home/username/repository/podi start
ExecStop=/home/username/repository/podi stop 
Type=forking

[Install]
WantedBy=multi-user.target default.target
```

and then run:

```
$ systemctl daemon-reload
$ systemctl start your-container
$ systemctl status your-container
(edit the service-file if it didn't work, and retry the 3 lines above)
$ systemctl enable your-container 
```

> voila..now it will persist across reboots
