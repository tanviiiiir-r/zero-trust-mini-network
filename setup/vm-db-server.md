# 🔹 DB Server VM Configuration

- **VM Name:** `db-server`
- **Region:** West Europe
- **Size:** B1s
- **Image:** Ubuntu 22.04 LTS
- **Subnet:** `db-subnet`
- **Public IP:** ❌ None
- **NSG:** `db-nsg`

## NSG Rules:
- Allow MySQL (port 3306) from `10.0.1.4` only (web-server)

![DB VM Overview](../screenshots/vm-overview-db.png)
![NSG DB Rules](../screenshots/nsg-db.png)