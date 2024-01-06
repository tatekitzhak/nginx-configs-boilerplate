## Nginx Configuration Boilerplate

Nginx is an event-driven webserver / reverse-proxy capable of handling many concurrent requests with relative ease.

### Nginx sample configuration files for common use cases:
- serving static files
- proxying 
- Advanced logging
- Backend response caching
- Optimized defaults
- Limiting

### Install Nginx on Amazon Linux 2 EC2 instance
- https://cloudkatha.com/how-to-install-nginx-on-amazon-linux-2-instance/
- https://stackoverflow.com/questions/57784287/how-to-install-nginx-on-aws-ec2-linux-2
- https://dev.to/0xfedev/how-to-install-nginx-as-reverse-proxy-and-configure-certbot-on-amazon-linux-2023-2cc9
- https://stackoverflow.com/questions/77579055/how-to-configure-nginx-in-amazon-linux-2023-based-ec2-instance-using-terraform

# -------- Tutors -----
- https://www.nginx.com/resources/wiki/start/topics/examples/full/
- https://docs.nginx.com/nginx/admin-guide/security-controls/securing-http-traffic-upstream/


NGINX config
- `sudo vim /etc/nginx/nginx.conf`
### 
- To help : `nginx -h`
- Version: `nginx -V` or `nginx -v`
- Check nginx runnig: `ps -ef | grep nginx`
- Check nginx status: `sudo systemctl status nginx`
- Use `sudo lsof -i TCP:80` to see what application is listening on port 80

### log
- `sudo tail -f /var/log/nginx/access.log`
- `sudo ls -l /var/log/nginx`
- Find the Nginx port as listed: `sudo netstat -tlpn| grep nginx`

### NGINX BASIC COMMAND
- `sudo systemctl enable nginx`
- `sudo systemctl status nginx` 
- `sudo systemctl restart nginx` 
- `sudo systemctl start nginx `
- `sudo systemctl stop nginx`
restart:
- `sudo systemctl restart nginx.service`
- `nginx -s reload`