=========================
Building mlvpn on OpenBSD
=========================

Installing requirements
=======================

.. code-block:: sh

    pkg_add git autoconf automake libev libsodium

Building mlvpn
==============

.. code-block:: sh

    export AUTOCONF_VERSION=2.69
    export AUTOMAKE_VERSION=1.14
    export CPPFLAGS="-I/usr/local/include $CPPFLAGS"
    export LDFLAGS="-L/usr/local/lib $LDFLAGS"
    git clone https://github.com/zehome/MLVPN mlvpn
    cd mlvpn
    ./autogen.sh
    ./configure
    make

Configuration
=============
Example configuration files for OpenBSD are located in **examples/mlvpn_updown_openbsd.sh**.
