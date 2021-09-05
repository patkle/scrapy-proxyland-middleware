# scrapy-proxyland-middleware
[![scrapy-proxyland-middleware on pypi](https://img.shields.io/pypi/v/scrapy-proxyland-middleware?color=blue)](https://pypi.org/project/scrapy-proxyland-middleware/)  
This middleware lets you use [Proxyland](https://proxyland.io) for every request you process with Scrapy.

## Settings
You need to specify your package credentials for Proxyland in your settings.py or settings object for this middleware to take effect. 

```python
PROXYLAND = {
    'username': 'package_username',
    'password': 'package_password'
}
```

You need to also enable ProxylandMiddleware as well as Scrapy's HttpProxyMiddleware. 

```python
DOWNLOADER_MIDDLEWARES = {
    'scrapy_proxyland_middleware.ScrapyProxylandMiddleware': 350,
    'scrapy.downloadermiddlewares.httpproxy.HttpProxyMiddleware': 400,
}
```
