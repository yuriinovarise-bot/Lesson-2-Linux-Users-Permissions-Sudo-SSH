# Lesson-2-Linux-Users-Permissions-Sudo-SSH
Created Linux users and groups, set file and directory permissions, configured sudo access, and set up secure SSH login. Practiced ACL, chmod, chown, and SSH keys. All steps documented and added to GitHub.

## Objectives
- Create and manage Linux users and groups
- Configure file and directory permissions using `chmod`, `chown`, and ACL
- Use `sudo` for administrative tasks
- Set up secure SSH access for local and remote users

## Users and Groups
- Created three users: `dev1`, `dev2`, `admin1`
- Created group: `developers`
- Added `dev1` and `dev2` to group `developers`
- Checked group membership using `id` and `groups` commands

## File and Directory Permissions
- Created directory `/home/dev1/project`
- Set owner-only permissions: `chmod 700 project`
- Gave group `developers` read and execute access: `setfacl -m g:developers:rx project`
- Created script file `script.sh` and set executable permission: `chmod +x script.sh`

## Sudo Configuration
- Added `admin1` to sudo group
- Verified `admin1` can execute commands as root: `sudo ls /root`
- Tested sudo command to create a directory in `/opt`

## SSH Setup
- Generated SSH key pair: `ssh-keygen -t rsa -b 4096`
- Copied public key to server: `ssh-copy-id user@localhost`
- Connected via SSH: `ssh dev1@localhost`
- Disabled root login by editing `/etc/ssh/sshd_config`

## Screenshots / Examples
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/fe863415-606c-4f28-b7f0-ea546d62f1f2" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6889ce15-f4bb-4071-b3f9-2c033ad50797" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/244c0ac8-2532-40d5-8f85-b8ff9be90144" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/13ff6738-4a5c-484c-884a-a6df2ec8b7de" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1b6f1440-6547-4698-b7f1-a7706174d78b" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f09b4908-0743-44d9-88a8-bf1dc98de763" />


## Notes
- Practiced all commands on multiple users
- Tested permissions and ACL thoroughly
- Documented all steps for reproducibility

