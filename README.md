# Docker Images

All images are published to the **GitHub Container Registry** and **Docker Hub**.

The images marked with `(DHI)` are based on the [Docker Hardened Image (DHI)](https://www.docker.com/products/hardened-images/) program and provide additional security features.

---

## How to use

Make sure to use the version with a datetime string as the suffix so that dependabot can recognize bugfix updates and notify you when they are available.
For example, use `ghcr.io/ventusforge/dhi-redis/8-2026.06.02.21.521` instead of `ghcr.io/ventusforge/dhi-redis:8`.

## Available images

> :warning: **Note:** The `dev` images are not intended for production use. They are only used for development and testing purposes.

### PHP

[![PHP](https://github.com/ventusforge/docker-images/actions/workflows/php.yml/badge.svg)](https://github.com/ventusforge/docker-images/actions/workflows/php.yml)


| Version          | Status             | Dockerfile                                                                |
|:-----------------|:-------------------|---------------------------------------------------------------------------|
| `8.5-fpm-alpine` | 🟢 **Stable**      | [ghcr.io/ventusforge/php/8.5-fpm-alpine](./php/8.5-fpm-alpine/Dockerfile) |
| `8.4-fpm-alpine` | 🟢 **Stable**      | [ghcr.io/ventusforge/php/8.4-fpm-alpine](./php/8.4-fpm-alpine/Dockerfile) |
| `8.3-fpm-alpine` | 🟢 **Stable**      | [ghcr.io/ventusforge/php/8.3-fpm-alpine](./php/8.3-fpm-alpine/Dockerfile) |

### Nginx (DHI)

[![Nginx](https://github.com/ventusforge/docker-images/actions/workflows/dhi-nginx.yml/badge.svg)](https://github.com/ventusforge/docker-images/actions/workflows/dhi-nginx.yml)


| Version        | Status        | Dockerfile                                                                        |
|:---------------|:--------------|-----------------------------------------------------------------------------------|
| `1-alpine`     | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-nginx/1-alpine](./dhi-nginx/1-alpine/Dockerfile)         |
| `1-alpine-dev` | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-nginx/1-alpine-dev](./dhi-nginx/1-alpine-dev/Dockerfile) |

### Traefik (DHI)

[![Traefik](https://github.com/ventusforge/docker-images/actions/workflows/dhi-traefik.yml/badge.svg)](https://github.com/ventusforge/docker-images/actions/workflows/dhi-traefik.yml)

| Version   | Status        | Dockerfile                                                                  |
|:----------|:--------------|-----------------------------------------------------------------------------|
| `3.7`     | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-traefik/3.7](./dhi-traefik/3.7/Dockerfile)         |
| `3.7-dev` | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-traefik/3.7-dev](./dhi-traefik/3.7-dev/Dockerfile) |
| `3.6`     | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-traefik/3.6](./dhi-traefik/3.6/Dockerfile)         |
| `3.6-dev` | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-traefik/3.6-dev](./dhi-traefik/3.6-dev/Dockerfile) |

### Redis (DHI)

[![Redis](https://github.com/ventusforge/docker-images/actions/workflows/dhi-redis.yml/badge.svg)](https://github.com/ventusforge/docker-images/actions/workflows/dhi-redis.yml)

| Version | Status        | Dockerfile                                                          |
|:--------|:--------------|---------------------------------------------------------------------|
| `8`     | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-redis/8](./dhi-redis/8/Dockerfile)         |
| `8-dev` | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-redis/8-dev](./dhi-redis/8-dev/Dockerfile) |

### MariaDB (DHI)

[![MariaDB](https://github.com/ventusforge/docker-images/actions/workflows/dhi-mariadb.yml/badge.svg)](https://github.com/ventusforge/docker-images/actions/workflows/dhi-mariadb.yml)

| Version  | Status        | Dockerfile                                                                |
|:---------|:--------------|---------------------------------------------------------------------------|
| `10`     | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-mariadb/10](./dhi-mariadb/10/Dockerfile)         |
| `10-dev` | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-mariadb/10-dev](./dhi-mariadb/10-dev/Dockerfile) |
| `11`     | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-mariadb/11](./dhi-mariadb/11/Dockerfile)         |
| `11-dev` | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-mariadb/11-dev](./dhi-mariadb/11-dev/Dockerfile) |
| `12`     | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-mariadb/12](./dhi-mariadb/12/Dockerfile)         |
| `12-dev` | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-mariadb/12-dev](./dhi-mariadb/12-dev/Dockerfile) |
| `13`     | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-mariadb/13](./dhi-mariadb/13/Dockerfile)         |
| `13-dev` | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-mariadb/13-dev](./dhi-mariadb/13-dev/Dockerfile) |
