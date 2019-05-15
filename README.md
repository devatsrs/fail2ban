# Fail2ban

Fail2ban installation and configuration.

## Installation

```
sudo yum install fail2ban
sudo systemctl enable  fail2ban
```

## Configuration

```
sudo cp /etc/fail2ban/jail.conf /etc/fail2ban/jail.local

sudo vi /etc/fail2ban/jail.local

```

## Change Configuration File

```
ignoreip = 127.0.0.1/8 117.247.87.0/32 78.129.239.0/32 137.59.230.0/32



[sshd]
enabled = true


[mysqld-auth]
enabled  = true

```
## Restart fail2ban

```
service fail2ban restart
```

## Check Configuration

```
[root@sd-151524 ~]# fail2ban-client status
Status
|- Number of jail:      2
`- Jail list:   mysqld-auth, sshd
[root@sd-151524 ~]#
```

