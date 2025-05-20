### 🔹 MySQL Configuration Verification

To enable remote access, follow these steps:

1. Edit MySQL config:

```bash
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
```

2. Change:

```ini
bind-address = 0.0.0.0
```

3. Restart MySQL:

```bash
sudo systemctl restart mysql
```

4. Verify it's listening:

```bash
sudo ss -tuln | grep 3306
```

Expected output:

```txt
LISTEN 0 80 0.0.0.0:3306
```

---

### 🔹 Connectivity Test Results

#### `ping.txt`

```txt
PING 10.0.2.4 (10.0.2.4): 56 data bytes
64 bytes from 10.0.2.4: icmp_seq=0 ttl=64 time=0.41 ms
64 bytes from 10.0.2.4: icmp_seq=1 ttl=64 time=0.33 ms
```

#### `nc.txt`

```txt
# Success
Connection to 10.0.2.4 port 3306 [tcp/mysql] succeeded!

# Failure (expected)
nc: connect to 10.0.2.4 port 22 (tcp) failed: Connection timed out
```

#### `mysql-connect.txt`

```txt
mysql -h 10.0.2.4 -u webapp -p
Welcome to the MySQL monitor...
mysql>
```
