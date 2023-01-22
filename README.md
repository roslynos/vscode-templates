# RoslynOS VS Code Template
This repository maintains the c# build template used in conjunction with the [RoslynOS Build System](https://github.com/roslynos/roslyn).  

## Enable SSH key authentication on RoslynOS device
```bash
# Use ssh-keygen on developemnt workstaton to create our SSH key pair and copy to device
ssh-keygen

# Update remote device with authorized keys. Replace with set hostname
cat ~/.ssh/id_rsa.pub | ssh gunshoe@rainier 'mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys'

# Secure the device public we transferred to authorized keys
chmod 700 .ssh
touch .ssh/authorized_keys
chmod 644 .ssh/authorized_keys
```