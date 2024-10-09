# Wazuh Deployment

Wazuh is an open-source security platform that provides security monitoring, threat detection, and incident response. Wazuh functions as a SIEM (Security Information and Event Management) solution that monitors logs, file integrity, malware analysis, and endpoint security across IT infrastructure. [More Info](https://documentation.wazuh.com/current/getting-started/index.html)

## Quickstart
### Set up a GCP instance to host the Wazuh dashboard.
![image](https://github.com/user-attachments/assets/329b1f1c-5727-4149-a0ab-56656a3bd5e7)

### Open SSH Cloud.
![image](https://github.com/user-attachments/assets/32f763f1-10b5-45b8-9d94-cf8ceb7ebaea)

### Installing Wazuh
Download and run the Wazuh installation assistant
```
curl -sO https://packages.wazuh.com/4.9/wazuh-install.sh && sudo bash ./wazuh-install.sh -a
```

![image](https://github.com/user-attachments/assets/78d28033-1399-4957-beed-a5e7b40fb0fb)

Once the assistant finishes the installation, the output shows the access credentials and a message that confirms that the installation was successful.
```
INFO: --- Summary ---
INFO: You can access the web interface https://<wazuh-dashboard-ip>
    User: admin
    Password: <ADMIN_PASSWORD>
INFO: Installation finished.
```

![image](https://github.com/user-attachments/assets/42a0830d-4488-471e-be0b-43aaed6bc0fe)
