[![Actions Status](https://github.com/frithnanth/perl6-Hash-Timeout/workflows/test/badge.svg)](https://github.com/frithnanth/perl6-Hash-Timeout/actions)

NAME
====

Hash::Timeout - Role for hashes whose elements timeout and disappear

SYNOPSIS
========

    use Hash::Timeout;

    my %cookies does Hash::Timeout[0.5];
    %cookies<user001> = 'id';
    sleep 1;
    say %cookies.elems; # prints 0

DESCRIPTION
===========

Hash::Timeout provides a `role` that can be mixed with a `Hash`.

There's just one optional parameter, the timeout, which accepts fractional seconds and defaults to 1 hour.

AUTHOR
======

Fernando Santagata <nando.santagata@gmail.com>

COPYRIGHT AND LICENSE
=====================

Copyright 2018 Fernando Santagata

This library is free software; you can redistribute it and/or modify it under the Artistic License 2.0.

