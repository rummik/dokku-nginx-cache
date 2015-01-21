 Dokku Nginx Cache [![Donations][]][gratipay]
===================
Wire in Nginx's proxy cache directives.

Tested with [Dokku-alt][].  Your milage may vary on vanilla Dokku.

[Donations]: http://img.shields.io/gratipay/rummik.png
[gratipay]: https://www.gittip.com/rummik/
[Dokku-alt]: https://github.com/dokku-alt/dokku-alt


### Installing
```
$ cd /var/lib/dokku-alt
$ git clone https://github.com/rummik/dokku-nginx-cache.git
```

### Quick start
Enable nginx request caching
```
$ dokku nginx:cache:enable my-app
```

Disable nginx request caching
```
$ dokku nginx:cache:disable my-app
```

### Configuration
Currently there are no configuration options.  However, Nginx does obey a
number of caching- and `X-Accel-*`-related headers.

Snippet from the [Nginx docs][]:

- `X-Accel-Expires`, `Expires`, `Cache-Control`, `Set-Cookie`, and `Vary` set
  the parameters of response [caching][];
- `X-Accel-Redirect` performs an [internal redirect][] to the specified URI;
- `X-Accel-Limit-Rate` sets the [rate limit][] for transmission of a response
  to a client;
- `X-Accel-Buffering` enables or disables [buffering][] of a response;
- `X-Accel-Charset` sets the desired [charset][] of a response.

[Nginx docs]: http://nginx.org/en/docs/http/ngx_http_proxy_module.html#proxy_ignore_headers
[caching]: http://nginx.org/en/docs/http/ngx_http_proxy_module.html#proxy_cache_valid
[internal redirect]: http://nginx.org/en/docs/http/ngx_http_core_module.html#internal
[rate limit]: http://nginx.org/en/docs/http/ngx_http_core_module.html#limit_rate
[buffering]: http://nginx.org/en/docs/http/ngx_http_proxy_module.html#proxy_buffering
[charset]: http://nginx.org/en/docs/http/ngx_http_charset_module.html#charset
