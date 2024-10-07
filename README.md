# Test EDA webhook
A repository to test Event Driven Ansible funtionalities using `ansible.eda.webhook`.

### Prerequisites
Open firewall ports on the EDA host to send payloads to port 5001/tcp.
```
firewall-cmd --permanent --add-port 5001/tcp
firewall-cmd --reload
```

### Testing
Run the payload on the webhook.
```
curl -H 'Content-Type: application/json' -d "{\"message\": \"Event Driven Ansible test webhook\"}" 127.0.0.1:5001/endpoint
```
