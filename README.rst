A simple buildout that builds varnish 4.1
=========================================

Installation
------------

source bin/activate
pip install -r requirements.txt
python bootstrap.py
bin/buildout

Activate a vhost
----------------

Add your host to the backends config in buildout.cfg:

[varnish-configuration]
recipe = plone.recipe.varnish:configuration
backends = starzel.de:localhost:8080
           portknox.net:loclhost:8090


More info
---------

Virtualhost https://info.varnish-software.com/blog/getting-virtual-hosts-right-varnish-cache
and https://www.getpagespeed.com/server-setup/varnish/varnish-virtual-hosts
