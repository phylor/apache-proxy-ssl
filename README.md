# Apache SSL Proxy in Docker

Provides apache in a docker container to be used as a proxy for SSL
sites.

Example for the proxy to listen on port 5000:

    docker run --rm -v /mycerts:/certs -v /mysites:/etc/apache2/sites-enabled -p 5000:443 phylor/apache-proxy-ssl

Provide SSL keys and certificates via a volume and reference them in
your configuration files using `/certs` as file location.
