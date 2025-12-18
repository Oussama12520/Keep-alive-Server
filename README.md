# Render Health Check HTTP Server

This is a lightweight HTTP server designed to keep your application alive on **Render** or similar hosting platforms that require periodic health checks.

## Purpose

Render and many other cloud hosting services automatically ping your service to make sure it is running. If the service does not respond to these pings, the platform may consider it unhealthy and restart it.  

This simple server responds to HTTP requests with a `200 OK` status, ensuring that your service is always recognized as healthy.

## Features

- Responds to HTTP `GET` requests with `200 OK` and a simple "OK" message.
- Responds to HTTP `HEAD` requests with `200 OK`.
- Listens on the port specified by the `PORT` environment variable (default is `10000`).
- Logs the port on which the server is running.

## Usage

1. Make sure Python is installed.
2. Set the `PORT` environment variable if you want to use a custom port.
3. Run the server:

```python
python your_server_file.py
