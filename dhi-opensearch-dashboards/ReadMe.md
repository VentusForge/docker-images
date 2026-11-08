# OpenSearch Dashboards Docker Hardened Image

Debian based. There is no Alpine variant in the DHI catalog, and no `-dev` variant.

- Runs rootless.
- Uses the nonprivileged user `opensearch-dashboards` (`1000:1000`)
- Runtime image has no shell and no package manager
- Listens on port 5601

[Read more](https://hub.docker.com/hardened-images/catalog/dhi/opensearch-dashboards/guides)
