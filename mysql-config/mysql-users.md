### 🔹 MySQL User Configuration

```sql
-- Create user for direct private IP access
CREATE USER 'webapp'@'10.0.1.4' IDENTIFIED BY 'SuperSecurePass!';
GRANT ALL PRIVILEGES ON *.* TO 'webapp'@'10.0.1.4';
FLUSH PRIVILEGES;

-- Create user for internal DNS-based access
CREATE USER 'webapp'@'web-server.internal.cloudapp.net' IDENTIFIED BY 'SuperSecurePass!';
GRANT ALL PRIVILEGES ON *.* TO 'webapp'@'web-server.internal.cloudapp.net';
FLUSH PRIVILEGES;
```

---

