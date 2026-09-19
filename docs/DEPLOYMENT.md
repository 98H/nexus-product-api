# Deployment & Operations Guide: Product API

## 🚀 Live Access & URLs
- **Live Public Access URL:** [/preview/prod-product-api-5f4406/](/preview/prod-product-api-5f4406/)
- **Internal Port:** `0`
- **Runtime Engine:** `python_preview`
- **Deployment Status:** `DEPLOYED / ACTIVE`
- **Timestamp:** `2026-09-19T16:19:18.307081+00:00`

## 🛠️ Management & Service Control
### Launch Command
```bash
python3 app.py --port 0
```

### Health Check Probe
```bash
curl -I http://127.0.0.1:0/
```

### Systemd Service Template
```ini
[Unit]
Description=Product API Service
After=network.target

[Service]
Type=simple
WorkingDirectory=/tmp/pytest-of-root/pytest-2/test_api_reset_and_control_end0/workspaces/prod-product-api-5f4406
ExecStart=/usr/bin/python3 /tmp/pytest-of-root/pytest-2/test_api_reset_and_control_end0/workspaces/prod-product-api-5f4406/app.py
Restart=always
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## 🔒 Production Security Protocols
- HTTP-only reverse proxy via Nexus Gateway.
- Dedicated port allocation with zero port conflict.
