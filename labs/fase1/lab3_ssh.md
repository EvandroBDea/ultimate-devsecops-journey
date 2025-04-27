📁 Lab 3 – Remote Connection Using SSH and Public Key

Goal: Establish passwordless SSH connection using a public key.

Commands:
ssh-keygen
ssh-copy-id user@remote_ip
ssh user@remote_ip

Generated file: ~/.ssh/id_rsa.pub copied to the remote server.
