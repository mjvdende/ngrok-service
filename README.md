# Description
Start ngrok tunnels as a systemd service. All ngrok files place in /opt/ngrok/..

# Example
1. Download [ngrok](https://ngrok.com/download) (/opt/ngrok/)
2. Put your authToken in ngrok.yml and copy to /opt/ngrok/
3. Copy ngrok.service to /etc/systemd/system/
4. Execute ```systemctl daemon-reload```
5. execute ```systemctl enable ngrok.service```

* Optional: change tunnel name /opt/ngrok/ngrok.yml 
```
tunnels:
  my-tunnel-name:
    proto: tcp
    addr: 22
```
and change tunnel in ngrok.service and ```systemctl restart ngrok.service```
