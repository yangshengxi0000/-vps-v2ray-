服务端程序地址：https://github.com/xueliqq/v2ray-heroku/blob/master/README.md
 v2ray客户端下载：https://github.com/v2ray/v2ray-core/releases
负载均衡配置文件路径：https://drive.google.com/file/d/16tnAMU1Lh82yIdAHKovJjV7QAtXoXhNE/view
我的负载均衡配置文件路径：https://drive.google.com/file/d/1AXmomHh8aK9aaq2sPiW8XMwmJYnoGm1v/view?usp=sharing
免费域名加速网站：https://dash.cloudflare.com/799cfe2809f103ade456e6626e9b1637










{
  "policy": null,
  "log": {
    "access": "",
    "error": "",
    "loglevel": "warning"
  },
  "inbounds": [
    {
      "tag": "proxy",
      "port": 10808,
      "listen": "127.0.0.1",
      "protocol": "socks",
      "sniffing": {
        "enabled": true,
        "destOverride": [
          "http",
          "tls"
        ]
      },
      "settings": {
        "auth": "noauth",
        "udp": true,
        "ip": null,
        "address": null,
        "clients": null
      },
      "streamSettings": null
    }
  ],
  "outbounds": [
    {
      "tag": "proxy",
      "protocol": "vmess",
      "settings": {
        "vnext": [
          {
            "address": "yugogogov.herokuapp.com",
            "port": 443,
            "users": [
              {
                "id": "ad806487-2d26-4636-98b6-ab85cc8521f7",
                "alterId": 64,
                "email": "t@t.tt",
                "security": "auto"
              }
            ]
          },
           {
            "address": "yugogogov1.herokuapp.com",
            "port": 443,
            "users": [
              {
                "id": "ad806487-2d26-4636-98b6-ab85cc8521f8",
                "alterId": 64,
                "email": "t@t.tt",
                "security": "auto"
              }
            ]
          }
      
            ]
          
        },
        "servers": null,
        "response": null,
      
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": true,
          "serverName": null
        },
        "tcpSettings": null,
        "kcpSettings": null,
        "wsSettings": {
          "connectionReuse": true,
          "path": "/",
          "headers": null
        },
        "httpSettings": null,
        "quicSettings": null
      },
      "mux": {
        "enabled": true,
        "concurrency": 8
      }
    },
    {
      "tag": "direct",
      "protocol": "freedom",
      "settings": {
        "vnext": null,
        "servers": null,
        "response": null
      },
      "streamSettings": null,
      "mux": null
    },
    {
      "tag": "block",
      "protocol": "blackhole",
      "settings": {
        "vnext": null,
        "servers": null,
        "response": {
          "type": "http"
        }
      },
      "streamSettings": null,
      "mux": null
    }
  ],
  "stats": null,
  "api": null,
  "dns": null,
  "routing": {
    "domainStrategy": "IPIfNonMatch",
    "rules": [
      {
        "type": "field",
        "port": null,
        "inboundTag": [
          "api"
        ],
        "outboundTag": "api",
        "ip": null,
        "domain": null
      }
    ]
  }
}



负载均衡配置文件.json
当前显示负载均衡配置文件.json。
