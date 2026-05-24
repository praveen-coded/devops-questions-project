# Question 1 - Set Up Your DevOps Project Structure

## Objective
Create the project directory structure, apply permissions, and ownership.

## Commands

```bash
mkdir -p /home/ec2-user/webapp/{scripts,logs,config}
```

Create config file:

```bash
cat > /home/ec2-user/webapp/config/app.conf
```

Add:

```text
APP_NAME=WebApp
PORT=8080
```

Press `Ctrl + D` to save.

Create log file:

```bash
touch /home/ec2-user/webapp/logs/app.log
ls -l /home/ec2-user/webapp/logs/app.log
```

Set permissions:

```bash
chmod 755 /home/ec2-user/webapp/scripts
chmod 644 /home/ec2-user/webapp/config/app.conf
```

Change ownership:

```bash
sudo chown -R root:root /home/ec2-user/webapp/
```

Verify:

```bash
ls -lR /home/ec2-user/webapp/
```
