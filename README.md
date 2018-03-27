erocksdb
========

[![Build Status](https://travis-ci.org/leo-project/erocksdb.svg?branch=develop)](http://travis-ci.org/leo-project/erocksdb)

Erlang bindings to [RocksDB](https://github.com/facebook/rocksdb) datastore.

This fork enhances portability using C++11 atomics and synchronization. This enables compilation on Windows (MSVC)

## Build Information

* "erocksdb" uses the [rebar](https://github.com/rebar/rebar) build system. Makefile so that simply running "make" at the top level should work.
* "erocksdb" requires Erlang R16B03-1 or later.

The fork is work in progress, the build scripts were not modified so building on Windows involves manual operations:
1. Build rocksdb (in any way)
2. Make a VS solution file, tweak the include and lib folders to match your setup
3. Build erocksdb.dll
4. Build the Erlang beam files

## Status

Limited testing on Windows (built with MSVC 2017).
Tested with [mnesia_eleveldb](https://github.com/klarna/mnesia_eleveldb). Used instead of [basho’s eleveldb](https://github.com/basho/eleveldb) backend. 

## Versioning

The release version follows the RocksDB's one.
For instance, if the version of erocksdb is 4.13.5 then the version of RocksDB erocksdb binds is also 4.13.5.

## License

erocksdb's license is [Apache License Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)

## Codebase

This code is based on [basho’s eleveldb](https://github.com/basho/eleveldb).

## Sponsors

LeoProject/LeoFS is sponsored by [Rakuten, Inc.](http://global.rakuten.com/corp/) and supported by [Rakuten Institute of Technology](http://rit.rakuten.co.jp/).
