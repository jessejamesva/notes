```markdown
# Apache Setup

1. Install Apache: `sudo dnf install -y httpd`
2. Enable & start service: `sudo systemctl enable --now httpd`
3. Verify status: `sudo systemctl status httpd`
4. Test in browser: `http://<your-ec2-ip>`

_Screenshot placeholder: screenshots/apache-test.png_
```
