SNI Proxy by dlundquist
=========

Proxies incoming HTTP and TLS connections based on the hostname contained in
the initial request of the TCP session. This enables HTTPS name-based virtual
hosting to separate backend servers without installing the private key on the
proxy machine.

News
----

This is just a deb build for me but others can use it pre-built

Features
--------
+ Name-based proxying of HTTPS without decrypting traffic. No keys or
  certificates required.
+ Supports both TLS and HTTP protocols.
+ Supports IPv4, IPv6 and Unix domain sockets for both back end servers and
  listeners.
+ Supports multiple listening sockets per instance.

Usage
-----

    Usage: sniproxy [-c <config>] [-f] [-n <max file descriptor limit>] [-V]
        -c  configuration file, defaults to /etc/sniproxy.conf
        -f  run in foreground, do not drop privileges
        -n  specify file descriptor limit
        -V  print the version of SNIProxy and exit


Installation
------------
```
wget https://github.com/txt3rob/sniproxy_ubuntu/raw/master/sniproxy_0.4.0_amd64.deb

wget https://github.com/txt3rob/sniproxy_ubuntu/raw/master/libudns0_0.4-1_amd64.deb

wget https://github.com/txt3rob/sniproxy_ubuntu/raw/master/libudns-dev_0.4-1_amd64.deb

dpkg -i libudns0_0.4-1_amd64.deb

dpkg -i libudns-dev_0.4-1_amd64.deb

apt-get install libev4 -y

dpkg -i sniproxy_0.4.0_amd64.deb




```

