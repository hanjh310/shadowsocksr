ShadowsocksR
===========

[![Build Status]][Travis CI]

A fast tunnel proxy that helps you bypass firewalls.

Server
------

### Install

Debian / Ubuntu:

    apt-get install git
    git clone https://github.com/shadowsocksr/shadowsocksr.git

CentOS:

    yum install git
    git clone https://github.com/shadowsocksr/shadowsocksr.git

Windows:

    git clone https://github.com/shadowsocksr/shadowsocksr.git

### Usage for single user on linux platform

If you clone it into "~/shadowsocksr"  
move to "~/shadowsocksr", then run:

    bash initcfg.sh

move to "~/shadowsocksr/shadowsocks", then run:

    python server.py -p 443 -k password -m aes-128-cfb -O auth_aes128_md5 -o tls1.2_ticket_auth_compatible

Check all the options via `-h`.

You can also use a configuration file instead (recommend), move to "~/shadowsocksr" and edit the file "user-config.json", then move to "~/shadowsocksr/shadowsocks" again, just run:

    python server.py

To run in the background:

    ./logrun.sh

To stop:

    ./stop.sh

To monitor the log:

    ./tail.sh

### Docker
docker pull hanjh/shadowsocksr

default env:

     ENV SERVER_ADDR     0.0.0.0
     ENV SERVER_PORT     8388
     ENV PASSWORD        pws
     ENV METHOD          aes-256-cfb
     ENV PROTOCOL        auth_sha1_v4
     ENV PROTOCOLPARAM   32
     ENV OBFS            http_post
     ENV TIMEOUT         300
     ENV DNS_ADDR        8.8.8.8
     ENV DNS_ADDR_2      8.8.4.4

Run docker:

     docker run -it -d -p443:8388  --name ssserver hanjh/shadowsocksr


you can change default env, example:

     docker run -it -d -p443:8388  -e PASSWORD=123456  --name ssserver hanjh/shadowsocksr



License
-------

Copyright 2015 clowwindy

Licensed under the Apache License, Version 2.0 (the "License"); you may
not use this file except in compliance with the License. You may obtain
a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
License for the specific language governing permissions and limitations
under the License.

Bugs and Issues
----------------

* [Issue Tracker]



[Android]:           https://github.com/shadowsocksr/shadowsocksr-android
[Build Status]:      https://travis-ci.org/shadowsocksr/shadowsocksr.svg?branch=manyuser
[Debian sid]:        https://packages.debian.org/unstable/python/shadowsocks
[iOS]:               https://github.com/shadowsocks/shadowsocks-iOS/wiki/Help
[Issue Tracker]:     https://github.com/shadowsocksr/shadowsocksr/issues?state=open
[OpenWRT]:           https://github.com/shadowsocks/openwrt-shadowsocks
[macOS]:             https://github.com/shadowsocksr/ShadowsocksX-NG
[Travis CI]:         https://travis-ci.org/shadowsocksr/shadowsocksr
[Windows]:           https://github.com/shadowsocksr/shadowsocksr-csharp
[Wiki]:              https://github.com/breakwa11/shadowsocks-rss/wiki
