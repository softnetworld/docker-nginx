# Docker Nginx
Nginx `Dockerfile` using Ubuntu 14.04 as base which provides:
- Nginx 1.6.2 (compiled from source).
- Host file system served Nginx config.
- Logging within container at `/var/log/nginx` (optionally passed back to host).
- Document root from host file system mounted within container at `/srv/http`.
- Ports `80` (HTTP) and `443` (HTTPS) exposed to host at `8080` / `8443` respectively.

## Usage
To build Docker image then run:

```
$ ./build.sh
$ ./run.sh \
	/path/to/nginx.conf \
	/path/to/docroot
```

To pass Nginx logs back to host:

```
$ ./run.sh \
	/path/to/nginx.conf \
	/path/to/docroot \
	/path/to/logs
```

Usable Nginx configuration example located under [nginx.conf/](nginx.conf).
