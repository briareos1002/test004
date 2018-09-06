gdstruct - GDS - General Data Structure
=======================================

A General Data Structure (GDS) is a universal, composable data structure, used to store any kind of data.   
This could be for example the definition of configurations, specifications and data sets.
Typical usage is the definition of configurations, specifications and data sets. 
The GDS language is a special DSL (domain specific language) for defining general data structures. 
It uses a succinct, indentation-sensitive syntax which makes data more readable. 
The building blocks for general data structures are hashes and arrays.

Installation
============

~~~
gem install gdstruct
~~~
  
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

The GDS language uses two basic symbols (__:__ and __,__) for the creation of hashes and arrays.

| __:__   | A colon is used to define a hash. |
| __,__   | A comma is used to define an array. |  

Use indentation with two spaces for the definition of elements and for nested structures. 
Tab characters are not allowed for indentation.

## General Example

~~~
,
  v1
  : k2 v2
  : k31 v31 | k32 v32 | k33 v33
    k34 v34
    k35 v35 | k36 v36 
  : 
    k41 v41
    k42 v42
    k43,
    k44, 1 | 2 | 3
      4 | 5
      6
      7
      8 | 9
      :k441 v441
  v5

# =>  [ 'v1', { k2: 'v2' }, { k31: 'v31', k32: 'v32', k33: 'v33', k34: 'v34', k35: 'v35', k36: 'v36' }, 
        { k41: 'v41', k42: 'v42', k43: [], k44: [1, 2, 3, 4, 5, 6, 7, 8, 9, { k441: 'v441' } ] }, 'v5' ] 
~~~

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
