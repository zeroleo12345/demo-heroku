## 概述

用于在 Heroku 上部署 V2Ray WebSocket

## 部署

### 添加环境变量

部署时需设定如下变量: [./entrypoint.sh](./entrypoint.sh)

| 变量名 | 建议值 | 说明 |
| :--- | :--- | :--- |
| `PORT` | `443` 或`80` | 监听端口 |
| `ID` | `7c76138d-5755-45eb-a4fd-eb5b2b7e3466` | VMess 用户主 ID，用于身份验证，为 UUID 格式 |
| `WSPATH` | `/` | WebSocket 所使用的 HTTP 协议路径 |

## 接入 CloudFlare

以下两种方式均可以将应用接入 CloudFlare，从而在一定程度上提升速度。

 1. 为应用绑定域名，并将该域名接入 CloudFlare
 2. 通过 CloudFlare Workers 反向代理

## 注意

 1. 若使用域名接入 CloudFlare，请考虑启用 TLS 1.3
