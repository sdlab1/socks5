# SOCKS5 Proxy Server

A lightweight, high-performance SOCKS5 proxy server implementation in Python with JSON-based user authentication.

## Features

- **SOCKS5 Protocol Support** - Full implementation with authentication
- **JSON User Management** - Easy user configuration via `users.json`
- **Multi-threaded** - Handles multiple concurrent connections
- **IPv4/IPv6 Support** - Works with both IP versions
- **Domain Resolution** - Supports domain name connections
- **High Performance** - Faster than HTTP proxies for most use cases

## Why SOCKS5?

SOCKS5 offers significant advantages over both SOCKS4 and HTTP proxies:

### vs SOCKS4
- ✅ **Authentication support** (SOCKS4 has none)
- ✅ **UDP traffic support** (SOCKS4 is TCP-only)
- ✅ **IPv6 compatibility** (SOCKS4 is IPv4-only)
- ✅ **Better security** through optional authentication
- ✅ **Modern protocol handling** for torrenting and gaming

### vs HTTP Proxy
- 🚀 **Faster performance** - Lower protocol overhead
- 🔄 **Any protocol support** - Not limited to HTTP/HTTPS
- 🎮 **Gaming & P2P friendly** - Better for real-time applications
- 📡 **UDP support** - Essential for DNS, VoIP, gaming
- 🔒 **Lower latency** - Direct TCP tunneling

## Quick Start

### 1. Setup
```bash
git clone <repository-url>
cd socks5-proxy
```

### 2. Configure Users
Create `users.json`:
```json
[
  {"username": "admin", "password": "secure123"},
  {"username": "user1", "password": "mypass456"}
]
```

### 3. Run Server
```bash
python server.py
```

Server starts on `127.0.0.1:1080`

### 4. Client Configuration
Configure your application to use:
- **Proxy Type**: SOCKS5
- **Host**: 127.0.0.1
- **Port**: 1080
- **Username/Password**: From your `users.json`

## Configuration

### Server Settings
Edit constants in `server.py`:
```python
SOCKS_ADDR = '127.0.0.1'  # Bind address
SOCKS_PORT = 1080         # Bind port
```

### User Management
Simply edit `users.json` and restart server:
```json
[
  {"username": "newuser", "password": "newpass"},
  {"username": "admin", "password": "adminpass"}
]
```

## Performance

SOCKS5 typically outperforms HTTP proxies because:
- **Lower overhead** - Minimal protocol wrapping
- **Direct tunneling** - Raw TCP/UDP passthrough
- **No content parsing** - Unlike HTTP proxies
- **Better for non-HTTP traffic** - Games, torrents, streaming

## Use Cases

- **Web Browsing** - Faster than HTTP proxy
- **Gaming** - Low latency, UDP support
- **Torrenting** - P2P traffic compatibility
- **Streaming** - Efficient media delivery
- **Development** - Testing geo-restricted APIs
- **Security** - Encrypted tunnel with authentication

## Supported Clients

Works with any SOCKS5-compatible application:
- Web browsers (Chrome, Firefox, Safari)
- Torrent clients (qBittorrent, Transmission)
- Games and gaming platforms
- Development tools (curl, wget)
- Mobile apps with proxy support

## Requirements

- Python 3.6+
- Standard library only (no external dependencies)

---

*Built for speed, security, and simplicity.*
