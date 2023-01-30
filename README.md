![Build](https://github.com/build-failure/nginx-naxsi/actions/workflows/main.yml/badge.svg)

# Nginx naxsi

Provides containerized Nginx reverse-proxy with [naxsi](https://github.com/nbs-system/naxsi).

Based on official [Nginx Docker image](https://hub.docker.com/_/nginx).

naxsi is build and included as a dynamic module according to the [repository documentation](https://github.com/nbs-system/naxsi/wiki/naxsi-compile).

# Supported Versions

Below the list of current supported version combinations between [Nginx](https://www.nginx.com/) and [naxsi](https://github.com/nbs-system/naxsi).

| Nginx | naxsi |
|---|---|
| 1.22.1 | 1.3 |

# Usage

See [Nginx Docker image documentation](https://hub.docker.com/_/nginx) for advanced usage examples.

    $ docker run --name some-nginx -v /some/content:/usr/share/nginx/html:ro -d nginx

# Test
For testing purposes use the nginx server [default.conf](test/etc/nginx/conf.d/default.conf) configuration file with [naxsi](https://github.com/nbs-system/naxsi) enabled.

[WAF Bypass Tool](https://github.com/nemesida-waf/waf-bypass) is used to analyze the WAF configuration to compare different WAFs.

    $ cd test
    $ docker-compose run waf-anylizer
    ...

# License

See the [LICENSE.md](LICENSE.md) file for details.
