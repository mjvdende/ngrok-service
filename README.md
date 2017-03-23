# Description
Start ngrok tunnels as a systemd service. All ngrok files place in /opt/ngrok/..

# Example
1. Copy ngrok.service to /etc/systemd/system/
2. Put your authToken in /opt/ngrok/ngrok.yml
3. Add tunell description to /opt/ngrok/ngrok.yml
```
tunnels:
  my-tunnel:
    proto: tcp
    addr: 22
```
4. Execute ```systemctl daemon-reload```
5. execute ```systemctl enable ngrok.service```
