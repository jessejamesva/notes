# MariaDB Setup

1. Install MariaDB: `sudo dnf install -y mariadb105-server`
2. Start & enable service: `sudo systemctl enable --now mariadb`
3. Secure installation: `sudo mysql_secure_installation`
4. Verify DB: `sudo systemctl status mariadb`

_Screenshot placeholder: screenshots/mariadb-setup.png_
