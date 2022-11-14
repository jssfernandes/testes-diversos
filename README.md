# testes-diversos

THE FIVE CONFIGURATION COMMANDS :
---------------------------------
1. sudo apt update && sudo apt upgrade -y
2. sudo apt-get install ubuntu-desktop xrdp stacer -y
3. sudo cp /etc/iptables/rules.v4 /etc/iptables/rules.v4.bak && sudo truncate -s 0 /etc/iptables/rules.v4
4. sudo rm /usr/share/polkit-1/actions/org.freedesktop.color.policy
5. sudo passwd ubuntu      Example password : t6y1Jx9n6h7j1  so long,complex and not in a dictionary

---

1. sudo add-apt-repository ppa:alessandro-strada/ppa
2. sudo apt update
3. sudo apt install google-drive-ocamlfuse
4. mkdir ~/googledrive
4.1	google-drive-ocamlfuse ~/googledrive
5. sudo nano /etc/systemd/system/google-drive.service
```
[Unit]
Description=FUSE filesystem over Google Drive
After=network.target

[Service]
User=ubuntu
Group=ubuntu
ExecStart=google-drive-ocamlfuse -label default /home/ubuntu/googledrive
ExecStop=fusermount -u /home/ubuntu/googledrive
Restart=always
Type=forking

[Install]
WantedBy=multi-user.target
Alias=google-drive.service
```

6. sudo systemctl daemon-reload
7. sudo systemctl start google-drive
8. sudo systemctl status google-drive



sudo apt-get install transmission-daemon
