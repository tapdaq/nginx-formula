=====
nginx
=====

Install nginx either by source or by package.

.. note::


    See the full `Salt Formulas installation and usage instructions
    <http://docs.saltstack.com/topics/conventions/formulas.html>`_.

Available states
================

.. contents::
    :local:

``nginx``
---------

Runs the states to install nginx, configure the common files, and the users.

``nginx.common``
----------------

Ensures standard nginx files are in place, and configures enabled sites.

``nginx.luajit2``
-----------------

Installs luajit.

``nginx.openresty``
-------------------

Installs openresty.

``nginx.package``
-----------------

Installs the nginx package via package manager.

``nginx.source``
----------------

Installs nginx via the source files.

``nginx.users``
---------------

Installs apache utils, and configures nginx users specified in the pillar.

Available templates
===================

Includes partials.

.. contents::
    :local:

``nginx/templates/config.site.jinja``
-------------------------------------

An extendible site-specific nginx config file that is meant to go into
``/etc/nginx/sites-*/``. Blocks available to be overwritten:

``port``
    Defaults to ``80``.

``server_name``
    Defaults to the FQDN of the minion, via the grain value.

``root``
    The absolute path to the document root. Defaults to ``/var/www/html``.

``path_404``
    The path to the 404 Not Found page. Defaults to ``/404.html``.

``footer``
    Custom configuration directives.
