### Open firewall ports on the EDA host
```
firewall-cmd --permanent --add-port 5001/tcp
firewall-cmd --reload
```

### Run the payload on the webhook
```
curl -H 'Content-Type: application/json' -d "{\"message\": \"Event Driven Ansible test webhook\"}" 127.0.0.1:5001/endpoint
```
