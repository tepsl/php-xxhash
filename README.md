PHP-xxHash
==========

A PHP extension to add support for the [xxHash](https://github.com/Cyan4973/xxHash) fast hashing algorithm.

[xxHash](https://github.com/Cyan4973/xxHash) is an Extremely fast Hash algorithm, running at RAM speed limits. 
It successfully completes the [SMHasher](http://code.google.com/p/smhasher/wiki/SMHasher) test suite which evaluates collision, dispersion and randomness qualities of hash functions.

## PHP5 Compatability

Please note the master branch should be used only for PHP 7.x

## Installation Instructions

```
   phpize
   ./configure --enable-xxhash
   make
   sudo make install
```
Don't forget to load the extension in via php.ini or the like.

## Usage Instructions

Upon installation and enabling the extension within php.ini the following two new functions will be available to you:

```
int xxhash32(string $data);
int xxhash64(string $data);
```

In both cases a int will be returned, representing the digest (hash) of the $data input.
Note that xxhash64 value is truncated to 32bit value in 32bit system.


## Credits
* Original implementation of [php-xxhash](https://github.com/Megasaxon/php-xxhash/) by Craig R.
* [xxHash](https://github.com/Cyan4973/xxHash) by Yann Collet.

## Licence

BSD 2-clause license.
