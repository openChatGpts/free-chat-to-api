# Free chat to api

[中文文档](README_CN.md)

## Features
- free chat to api
- free chat gateway

## Installation
```bash
docker run -d -p 8484:8484 --name free-chat-to-api ghcr.io/zbronya/free-chat-to-api:latest
```

## Usage
```bash
curl 'http://127.0.0.1:8484/v1/chat/completions' \
--header 'Content-Type: application/json' \
--data '{
    "model": "gpt-3.5-turbo",
    "messages": [
        {
            "role": "user",
            "content": "Say this is a test! "
        }
    ],
    "stream": true
}'
```

## Environment Variables
- `PORT` - port to listen on (default: `8484`)
- `BIND` - address to bind to (default: `0.0.0.0`)
- `PROXY_URL` - proxy url
- `GATEWAY_URL` - gateway url (default: `https://chatgpt.com`)

## What's next
- [使用TunnelBroker提供的免费/48的ipv6解决chat-to-api的429问题](https://bronya.io/chat-to-api-solving-429/)
