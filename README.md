Rails 1.9.3 Ubuntu Lucid Packages (Backports)
=============================================

Quick ugly notes
----------------

* Basically changed the debhelper dependency on `ruby1.9.1_1.9.3.0-1ubuntu2.dsc` and `debian/control` 

* Change in `debian/compat` from 9 to 7

* Finally `dpkg-buildpackage -rfakeroot -uc -b` 

