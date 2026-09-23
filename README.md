# vps
https://www.youtube.com/watch?v=zWnCQVzM_Bw&t=1136s
```bash <(curl -fsSL https://raw.githubusercontent.com/hopingboyz/vms/main/vm.sh)```
 ```git clone https://github.com/Flaxmc1/hvm```

``` cd hvm ```
```apt update && apt install unzip -y && apt install snapd -y && sudo snap install lxd -y && apt install python3-pip```
```unzip hvm.zip```
```cd hvm```
```pip install flask && pip install flask_login && pip install paramiko```
```echo 'export PATH=$PATH:/snap/bin' >> /root/.bashrc```
```source /root/.bashrc```
```lxd init ```
```nano /etc/systemd/system/hvm.service```

```[Unit]
Description=HVM Python Service
After=network.target

[Service]
Type=simple
ExecStart=/usr/bin/python3 /root/hvm/hvm/hvm.py
WorkingDirectory=/root/hvm/hvm
Restart=always
User=root

[Install]
WantedBy=multi-user.target```


 ```systemctl deamon-reload```
```systemctl start hvm  ```
