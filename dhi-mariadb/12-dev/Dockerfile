FROM dhi.io/mariadb:12-debian13-dev

# Patch gawk (CVE-2026-40468, CVE-2026-40469) until the base image ships the fixed version
USER root
RUN apt-get update \
    && apt-get install -y --only-upgrade --no-install-recommends gawk \
    && rm -rf /var/lib/apt/lists/*
