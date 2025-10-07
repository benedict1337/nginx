# 🚀 NGINX Docker Image

A **lightweight NGINX Docker image**, optimized for modern web protocols, high performance, and enhanced security.  

![Docker Pulls](https://img.shields.io/docker/pulls/benedicthu/nginx) ![Docker Image Size](https://img.shields.io/docker/image-size/benedicthu/nginx/latest) [![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/) ![HTTP/3](https://img.shields.io/badge/HTTP-3-4CAF50)

---

## ✨ Key Features

- 🚀 **HTTP/3 (QUIC)** and **0-RTT** support for faster connections  
- ⚡ Dynamic **TLS record patching**  
- 📦 **Brotli compression** for optimized content delivery  
- 🌍 **GeoIP2** support for geolocation-based features  
- 📝 **NJS** scripting support  
- 🛡️ **ModSecurity** WAF integration  

> ⚠️ **Note:** Make sure UDP port 443 is open on your host for HTTP/3.  

---

## 🏃 Quick Start

### Using `docker run`

```bash
docker run -d \
  --restart unless-stopped \
  -p 80:80 \
  -p 443:443 \
  -p 443:443/udp \
  -v nginx-config:/etc/nginx \
  benedicthu/nginx
```

### Using Docker Compose
```yaml
version: '3.9'

services:
  nginx:
    image: benedicthu/nginx
    volumes:
      - 'nginx-config:/etc/nginx'
    ports:
      - '80:80'
      - '443:443'
      - '443:443/udp'
    restart: unless-stopped
```

---

## 📄 License

This project is licensed under GPLv3 License.