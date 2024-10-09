# Wazuh Deployment

Wazuh is an open-source security platform that provides security monitoring, threat detection, and incident response. Wazuh functions as a SIEM (Security Information and Event Management) solution that monitors logs, file integrity, malware analysis, and endpoint security across IT infrastructure. [More Info](https://documentation.wazuh.com/current/getting-started/index.html)

## Quickstart
### Set up a GCP instance to host the Wazuh dashboard.
![image](https://github.com/user-attachments/assets/f24e3da2-c360-40ac-bbd9-adec468adb54)


### Installing Wazuh
Download and run the Wazuh installation assistant
```
curl -sO https://packages.wazuh.com/4.9/wazuh-install.sh && sudo bash ./wazuh-install.sh -a
```

