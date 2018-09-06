gdstruct - GDS - General Data Structure
=======================================

A General Data Structure (GDS) is used to store any kind of data. 
This could be for example the definition of configurations, specifications and data sets.

Installation
============

    gem install gdstruct
  
A Short Example
===============

~~~ruby
require "gdstruct"

h = GDstruct.c( <<-EOS )
:
  a val a
  b val b
EOS

# => h = { a: 'val a', b: 'val b' }
~~~


An Introduction
===============

Futher Information
==================

You will find futher information here [https://urasepandia.de/gds.html](https://urasepandia.de/gds.html)

Maintainer
==========

Uli Ramminger <uli@urasepandia.de>

Copyright
=========

Copyright (c) 2018 Ulrich Ramminger

See MIT-LICENSE for further details.
