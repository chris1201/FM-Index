FM-Index - Compressed full-text Index
=====================================

A simple c++ FM-Index [1] implementation using RRR [4] wavelet trees [5]
which allows to build a full-text index over a given text `T` supporting the
following operations:

  * `count(P)`     : count the number of occurences of `P` in `T`.
  * `locate(P)`    : locate the text positions of all occurences of `P` in `T`.
  * `display(A,B)` : extract `T[A,B]` 
  
Usage
-----

### Command Parameters

	./fm-index
	USAGE: ./fm-index -i <index> -q <queries> -k <depth> -s <samplerate> -r -l -d <input>
		-i index file
		-d input file
		-q query file
		-s samplerate [default = 64]
		-l locate occurrences
		-r recover original text

### Examples
		
Testing
-------

TODO
 
Benchmarks
----------


Libraries
---------

The following libraries are needed to use the index. Sourcecode for both
libaries is included.

 * [.libcds](http://libcds.recoded.cl/) -- succinct low level data structures
 * [.libdivsufsort(http://code.google.com/p/libdivsufsort/) -- fast suffix sorting

Licence
--------

GPL v3

References
-----------

 * Paolo Ferragina and Giovanni Manzini. Indexing compressed text. Journal of the ACM, 52(4):552-581, 2005.
 * Francisco Claude and Gonzalo Navarro. Practical Rank/Select Queries over Arbitrary Sequences. Proc. SPIRE'08 176-187, 2008.
 * Veli M�kinen and Gonzalo Navarro. Implicit Compression Boosting with Applications to Self-Indexing. Proc. SPIRE'07 214-226.
 * R. Raman, V. Raman, and S. Srinivasa Rao. Succinct indexable dictionaries with applications to encoding k-ary trees and multisets. In SODA'02, 233�242.
 * R. Grossi, A. Gupta, and J. Vitter. High-order entropy-compressed text indexes. In SODA'03, 841�850.
 