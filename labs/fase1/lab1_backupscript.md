📁 Lab 1 – Backup Script with cron

Goal: Create an automated backup script using cron.

Location: /linux/scripts/backup.sh

Description:
#!/bin/bash
tar -czf ~/backup_home_$(date +%F).tar.gz /home/evandro

Scheduled with crontab:
0 2 * * * /home/evandro/scripts/backup.sh

