## Multiarch [Docker](https://docker.com) image for [Caddy](https://caddyserver.com)


### Installed packages

- bash
- ca-certificates
- curl
- openssl
- git (for caddy git plugin)
- openssh-client

- [caddy](https://caddyserver.com)
- [hugo](https://gohugo.io)

And for debugging:
- bind-tools
- drill

### Eabled caddy features
- DNS
- git
- hugo
- cors
- filemanager
- ipfilter
- jwt
- locale
- minify
- ratelimit
- realip
- upload

### Usage

##### Run as DNS server 
`docker run -d --name dns -p 53:53 -p 53:53/udp firecyberice/caddy:latest`

##### Run as web server
`docker run -d --name dns -p 80:80 -p 443:443 -p 2015:2015 firecyberice/caddy:latest`


### Build

`docker build -t firecyberice/caddy:amd64 -f Dockerfile:amd64 .`

`docker build -t firecyberice/caddy:arm -f Dockerfile:arm .`

***Note*** There are some build args available:

- CADDY_FEATURES `--build-arg CADDY_FEATURES="cors,ipfilter,minify,realip"`
- HUGO_VERSION  `--build-arg HUGO_VERSION=0.18.1`
