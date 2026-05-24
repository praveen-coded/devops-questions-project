# Question 3 - User Management and File Permission Control

## Create Group

```bash
sudo groupadd writers
```

## Create Users

```bash
sudo useradd -m devuser1
sudo useradd -m devuser2
sudo useradd -m devuser3
sudo useradd -m devuser4
```

## Set Passwords

```bash
sudo passwd devuser1
sudo passwd devuser2
sudo passwd devuser3
sudo passwd devuser4
```

## Add Writers Group Access

```bash
sudo usermod -aG writers devuser1
sudo usermod -aG writers devuser2
```

## Change Ownership

```bash
sudo chown root:writers /home/ec2-user/webapp/scripts/log_user.sh
```

## Set Permissions

```bash
sudo chmod 664 /home/ec2-user/webapp/scripts/log_user.sh
```

## Verify

```bash
ls -l /home/ec2-user/webapp/scripts/log_user.sh
```

## Test Access

Writer user:

```bash
su - devuser1
echo "test" >> /home/ec2-user/webapp/scripts/log_user.sh
```

Read-only user:

```bash
su - devuser3
cat /home/ec2-user/webapp/scripts/log_user.sh
echo "test" >> /home/ec2-user/webapp/scripts/log_user.sh
```
