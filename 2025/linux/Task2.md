# Task: File and Directory Permissions in Linux

```bash
# 1. Create /devops_workspace directory
sudo mkdir /devops_workspace

# 2. Create project_notes.txt inside /devops_workspace
sudo touch /devops_workspace/project_notes.txt

# 3. Set ownership to the current user
sudo chown $USER:$USER /devops_workspace/project_notes.txt

# 4. Set permissions:
#    - Owner: Read & Write
#    - Group: Read-only
#    - Others: No access
sudo chmod 640 /devops_workspace/project_notes.txt

# 5. Verify permissions
ls -l /devops_workspace/project_notes.txt
