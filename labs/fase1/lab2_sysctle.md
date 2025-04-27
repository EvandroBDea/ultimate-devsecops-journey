📁 Lab 2 – Service Management with systemctl and Logs with journalctl

Goal: Activate, restart, and view logs for the SSH service.

Commands used:
sudo systemctl status ssh
sudo systemctl restart ssh
sudo systemctl enable ssh
journalctl -u ssh -b
journalctl -xe | grep ssh

Description: Practical test of managing services with systemd,
including reading and analyzing logs.
