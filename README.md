Rails 1.9.3 Ubuntu Lucid Packages (Backports)
=============================================

Dependencies
------------

For `libtcltk-ruby` : 

* `apt-get install tk8.4 tcl8.4`

For `libruby`

* `apt-get install libffi5 libyaml-0-2`

One-Liner: 

* `apt-get install tk8.4 tcl8.4 libffi5 libyaml-0-2`

Full Ruby 1.9.3 install: 
------------------------

Just call `dpkg -i ruby1.9.1-full_1.9.3.0-1ubuntu2_all.deb`, or, with all dependencies:

* `dpkg -i ruby1.9.1-full_1.9.3.0-1ubuntu2_all.deb ri1.9.1_1.9.3.0-1ubuntu2_all.deb libruby1.9.1_1.9.3.0-1ubuntu2_i386.deb ruby1.9.1-dev_1.9.3.0-1ubuntu2_i386.deb ruby1.9.1-examples_1.9.3.0-1ubuntu2_all.deb libruby1.9.1-dbg_1.9.3.0-1ubuntu2_i386.deb ruby1.9.3_1.9.3.0-1ubuntu2_all.deb ruby1.9.1_1.9.3.0-1ubuntu2_i386.deb  libtcltk-ruby1.9.1_1.9.3.0-1ubuntu2_i386.deb 
`

It will install ruby 1.9.3 as default and gem 1.8.11: 

* `# ruby -v
ruby 1.9.3p0 (2011-10-30 revision 33570) [i486-linux]`

* `# gem -v
1.8.11`


Quick'n'ugly build notes
------------------------

* Get the source from 12.04 (apt-get source blahblah)
* Basically changed the debhelper useless version dependency on `ruby1.9.1_1.9.3.0-1ubuntu2.dsc` and `debian/control` 

* Change in `debian/compat` from 9 to 7

* Finally build it: `dpkg-buildpackage -rfakeroot -uc -b` 

