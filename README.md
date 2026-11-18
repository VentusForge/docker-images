# Docker Images

All images are published to the **GitHub Container Registry** and **Docker Hub**.

The images marked with `(DHI)` are based on the [Docker Hardened Image (DHI)](https://www.docker.com/products/hardened-images/) program and provide additional security features.

---

## How to use

Pin the tag that carries the build timestamp so that Dependabot can recognize new builds and propose them as updates.
For example, use `ghcr.io/ventusforge/dhi-redis:8.0.0.202611180207` instead of `ghcr.io/ventusforge/dhi-redis:8`.

### Tag format

Every build gets a tag in the format `<major>.<minor>.<patch>.<YYYYMMDDHHMM>[-<variant>][-dev]` (UTC). Missing version parts are filled with `0`, so `8` becomes `8.0.0.<timestamp>`. The `0` parts are placeholders and do not stand for a specific bugfix release:

| Image directory   | Timestamp tag                   |
|:------------------|:--------------------------------|
| `8`               | `8.0.0.202611180207`            |
| `8-dev`           | `8.0.0.202611180207-dev`        |
| `1-alpine`        | `1.0.0.202611180207-alpine`     |
| `1-alpine-dev`    | `1.0.0.202611180207-alpine-dev` |
| `8.4-fpm-alpine`  | `8.4.0.202611180207-fpm-alpine` |

Dependabot only compares tags with the same suffix and sorts them by the numeric part, which is why the timestamp is part of the version and never of the suffix.

- A normal tag only receives updates to newer normal tags of the same variant.
- A `-dev` tag only receives updates to newer `-dev` tags of the same variant. Dependabot treats `-dev` tags as pre-releases, so a normal tag is never updated to a `-dev` tag.
- A timestamp update is always a patch update for Dependabot. An `ignore` rule for `version-update:semver-patch` in your `dependabot.yml` therefore hides these updates.

> **Note:** Tags with a dotted timestamp (e.g. `8.0.0.2026.11.18.02.07-dev`) are updated to the current format automatically. Tags in the format `8-2026.06.02.21.52` and tags with the timestamp in the suffix (e.g. `1.0.0-alpine.2026.09.06.02.07` or `8.0.0-dev.2026.09.06.02.07`) cannot be compared with the current format. Update such a tag once by hand to a current timestamp tag. From then on Dependabot proposes new builds automatically.

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
| `13`     | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-mariadb/13](./dhi-mariadb/13/Dockerfile)         |
| `13-dev` | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-mariadb/13-dev](./dhi-mariadb/13-dev/Dockerfile) |

### Alpine Base (DHI)

[![Alpine Base](https://github.com/ventusforge/docker-images/actions/workflows/dhi-alpine.yml/badge.svg)](https://github.com/ventusforge/docker-images/actions/workflows/dhi-alpine.yml)

| Version    | Status        | Dockerfile                                                                  |
|:-----------|:--------------|-----------------------------------------------------------------------------|
| `3.24`     | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-alpine/3.24](./dhi-alpine/3.24/Dockerfile)         |
| `3.24-dev` | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-alpine/3.24-dev](./dhi-alpine/3.24-dev/Dockerfile) |

### OpenSearch

[![OpenSearch](https://github.com/ventusforge/docker-images/actions/workflows/dhi-opensearch.yml/badge.svg)](https://github.com/ventusforge/docker-images/actions/workflows/dhi-opensearch.yml)

| Version          | Status        | Dockerfile                                                                                      |
|:-----------------|:--------------|-------------------------------------------------------------------------------------------------|
| `3.9-debian`     | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-opensearch/3.9-debian](./dhi-opensearch/3.9-debian/Dockerfile)         |
| `3.9-debian-dev` | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-opensearch/3.9-debian-dev](./dhi-opensearch/3.9-debian-dev/Dockerfile) |

### OpenSearch Dashboards

[![OpenSearch Dashboards](https://github.com/ventusforge/docker-images/actions/workflows/dhi-opensearch-dashboards.yml/badge.svg)](https://github.com/ventusforge/docker-images/actions/workflows/dhi-opensearch-dashboards.yml)

| Version          | Status        | Dockerfile                                                                                                            |
|:-----------------|:--------------|-----------------------------------------------------------------------------------------------------------------------|
| `3.9-debian`     | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-opensearch-dashboards/3.9-debian](./dhi-opensearch-dashboards/3.9-debian/Dockerfile)         |

### Eclipse MQTT

[![MQTT](https://github.com/ventusforge/docker-images/actions/workflows/dhi-mqtt.yml/badge.svg)](https://github.com/ventusforge/docker-images/actions/workflows/dhi-mqtt.yml)

| Version      | Status        | Dockerfile                                                                  |
|:-------------|:--------------|-----------------------------------------------------------------------------|
| `2.1-debian` | 🟢 **Stable** | [ghcr.io/ventusforge/dhi-mqtt/2.1-debian](./dhi-mqtt/2.1-debian/Dockerfile) |
