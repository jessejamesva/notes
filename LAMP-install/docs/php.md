# PHP Setup

1. Install PHP and MySQL module: `sudo dnf install -y php php-mysqli php-cli`
2. Restart Apache: `sudo systemctl restart httpd`
3. Verify PHP with info page:

```bash
echo "<?php phpinfo(); ?>" | sudo tee /var/www/html/info.php
```

4. Visit `http://<your-ec2-ip>/info.php`

_Screenshot placeholder: screenshots/php-info.png_
