# Install Ubuntu 20.04
```
wget https://repo.zabbix.com/zabbix/6.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_6.0-4+ubuntu20.04_all.deb
sudo dpkg -i zabbix-release_6.0-4+ubuntu20.04_all.deb
sudo apt update
sudo apt install zabbix-agent -y
sudo nano /etc/zabbix/zabbix_agentd.conf

Cập nhật các tham số sau:
- Server: IP của Zabbix Server.
- ServerActive: IP của Zabbix Server (cho các item dạng active check).
- Hostname: Tên định danh của host này trên Zabbix Web UI.

sudo systemctl restart zabbix-agent
sudo systemctl enable zabbix-agent
sudo ufw allow 10050/tcp
```
