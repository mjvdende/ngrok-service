# Description
Start ngrok tunnels as a systemd service. All ngrok files place in /opt/ngrok/..

# Example
1. Copy ngrok.service to /etc/systemd/system/
Put your authToken in /opt/ngrok/ngrok.yml
2. Add tunell description to /opt/ngrok/ngrok.yml
```
tunnels:
  my-tunnel:
    proto: tcp
    addr: 22
```
3. Execute ```systemctl daemon-reload```
4. execute ```systemctl enable ngrok.service```
