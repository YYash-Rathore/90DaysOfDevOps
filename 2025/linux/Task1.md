
# Linux User and Group Management

```bash
# 1. Create a User devops_user
sudo useradd -m devops_user -s /bin/bash

# 2. Create a Group devops_team
sudo groupadd devops_team

# 3. Add devops_user to devops_team
sudo usermod -aG devops_team devops_user
sudo gpasswd -a devops_user devops_team

# 4. Set a Password for devops_user
sudo passwd devops_user

# 5. Grant Sudo Access to devops_user
sudo usermod -aG sudo devops_user
visudo
devops_user ALL=(ALL) NOPASSWD:ALL

# 6. Restrict SSH Login for Certain Users
sudo nano /etc/ssh/sshd_config

# Add these lines at the end of the file
DenyUsers user1 user2
AllowUsers devops_user admin

# Restart SSH service
sudo systemctl restart sshd
```

