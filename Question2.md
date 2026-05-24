# Question 2 - Interactive Log Script

## Navigate

```bash
cd /home/ec2-user/webapp/scripts/
```

## Create Script

```bash
vim log_user.sh
```

Press `i` and paste:

```bash
#!/bin/bash

read -p "Enter your name: " username

cat /home/ec2-user/webapp/config/app.conf

echo "Login: $username Date: $(date)" >> /home/ec2-user/webapp/logs/app.log

cat /home/ec2-user/webapp/logs/app.log
```

Save:

```text
Esc
:wq
```

Make executable:

```bash
chmod +x log_user.sh
```

Run:

```bash
./log_user.sh
```

Check logs:

```bash
cat /home/ec2-user/webapp/logs/app.log
```
