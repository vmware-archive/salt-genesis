==============
SLS Generators
==============

Most Unix/Linux distributions these days support some sort of automated install
method. For example, RedHat-based distros use Kickstart files, Debian uses
Preseed files, and SUSE uses AutoYAST. Several fine utilities already exist to
generate these files for you. Why not put them to work with Salt?

One of the many functions that Salt features is configuration management. Salt
uses SLS files to provision systems, and mitigate confguration drift. If you're
using a system that was installed just the way you want using Anaconda, you
probably already have a basic set of configuration, which can be used as the
baseline for your Salt configuration.

Upon successful installation of a system, Anaconda places a file on the system
that describes how it was installed.

.. code-block:: bash

    -rw-------. 1 root root 1234 Mar 11 11:38 /root/anaconda-ks.cfg

This file can be easily converted to an SLS file using kickstart2sls. There are
also scripts for Debian (preseed2sls) and SUSE (autoyast2sls).

These scripts are nowhere near completion, and currently only kickstart2sls
can be said to be in any usable state. Keep posted for updates.
