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
