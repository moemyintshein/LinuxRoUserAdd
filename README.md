# LinuxRoUserAdd
New user add with specific directory read only, add ssh public key

1. Update inventory.ini with your hosts and ansible remote user (user shoule be sudo password less)

2. Update vars.json with actual value
   - username
   - user_password  #<- Replace with hashed password (mkpasswd --method=SHA-512)
   - ssh_public_key

3. Run ansible-playbook with extra variable
```
ansible-playbook -i inventory.ini create_user.yml -e "@vars.json"
```
