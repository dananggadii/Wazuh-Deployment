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

### Login Wazuh Dashboard
![image](https://github.com/user-attachments/assets/42a0830d-4488-471e-be0b-43aaed6bc0fe)

### Open the menu on the sidebar || Server Management || Endpoints summary
![image](https://github.com/user-attachments/assets/baa8d070-6cba-4e40-9129-9c72e3579a38)

### Create a GCP instance for the Wazuh Agent.
![image](https://github.com/user-attachments/assets/4fce0360-3ac0-49cf-abdd-152acaa02f98)

### Open SSH Cloud.
![image](https://github.com/user-attachments/assets/104d0c60-3724-4913-9e22-76d4d48d1c9b)

### Add the Wazuh repository
* Install the GPG key:
  ```
  curl -s https://packages.wazuh.com/key/GPG-KEY-WAZUH | gpg --no-default-keyring --keyring gnupg-ring:/usr/share/keyrings/wazuh.gpg --import && chmod 644 /usr/share/keyrings/wazuh.gpg
  ```
* Add the repository:
  ```
  echo "deb [signed-by=/usr/share/keyrings/wazuh.gpg] https://packages.wazuh.com/4.x/apt/ stable main" | tee -a /etc/apt/sources.list.d/wazuh.list
  ```
* Update the package information:
  ```
  apt-get update
  ```
