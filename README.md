# webstack

**Webstack** is a staging / production *nix web server configuration package. It aims to provide well optimized configuration files for web servers with a minimum painful setup.

It currently includes config files for:

* nginx (v1.2.5 tested)
* uwsgi (v1.4.2 tested)
* php (v5.4.8 tested with php-fpm)
* mongodb (not tested yet)

It **does not** install these software mentioned above but collects their config and log files in one place. Currently, `/data` folder is being used almost for everything. Such folders should be created:

* `/data/webstack` for this package
* `/data/log` for the log files, also application specific sub-folders (i.e. `/data/log/nginx`)
* `/data/env` for Python virtualenv root
* `/data/env/myproject/app` symbolic link to the project's application directory (see below)
* `/data/app` for projects directory (i.e. `/data/app/myproject`)


You may also need to create symbolic links one-by-one under your `/etc/default` (to `/data/webstack/etc/default`) directory to specify where all the configs files to these daemons.

It is currently **beta**, may cause unexpected results. Use at your own risk.
