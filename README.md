# nginx-http-flv-module-packages
Some rpm packages for [nginx-http-flv-module](https://github.com/winshining/nginx-http-flv-module).

[nginx-http-flv-module](https://github.com/winshining/nginx-http-flv-module) is built as a dynamic module in this project and now only rpm packages for Red Hat Enterprise Linux 6 (CentOS 6) and 7 (CentOS 7) are available.

# Prerequisites

* [Nginx](http://nginx.org) installed via yum on Red Hat Enterprise Linux 6 (CentOS 6) or 7 (CentOS 7).

# Install

    rpm -ivh nginx-http-flv-module-version-release.arch.rpm

For example, on Red Hat Enterprise Linux 6 (CentOS 6), you can install [nginx-http-flv-module](https://github.com/winshining/nginx-http-flv-module) via:

    rpm -ivh nginx-http-flv-module-1.2.4-1.el6.x86_64.rpm

## Note

You must run as root to install rpm packages.

# After installation

## Add conf files into nginx.conf

conf files used by [nginx-http-flv-module](https://github.com/winshining/nginx-http-flv-module) now is located in /etc/nginx/http-flv, you can `include` them in /etc/nginx/nginx.conf:

    http {
        ...;
        include /etc/nginx/http-flv/http-flv.conf;
    }

    include /etc/nginx/http-flv/rtmp.conf;

### Note

Before `include` conf files, you can modify them according to your environment.

## Start or reload [Nginx](http://nginx.org)

    service nginx start

or

    service nginx reload
