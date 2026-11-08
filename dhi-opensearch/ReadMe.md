# OpenSearch Docker Hardened Image

Debian 13 based. There is no Alpine variant in the DHI catalog.

- Runs rootless.
- Uses the nonprivileged user `opensearch` (`1000:1000`)
- Runtime image has no shell and no package manager
- Use the `-dev` variant to install extra plugins
- Listens on ports 9200 (REST), 9300 (transport), 9600 (Performance Analyzer), and 9650

[Read more](https://hub.docker.com/hardened-images/catalog/dhi/opensearch/guides)