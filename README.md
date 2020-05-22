# Bytestrings

This is an implementation of a
[pre-SRFI specification](https://bitbucket.org/cowan/r7rs-wg1-infra/src/default/BytestringsCowan.md)
by John Cowan which provides bytestrings for Scheme.  It should be
portable to any R7RS-small implementation with
[SRFI 1/(scheme list)](https://srfi.schemers.org/srfi-1) and
[SRFI 151/(scheme bitwise)](https://srfi.schemers.org/srfi-151).  In
addition, [SRFI 145](https://srfi.schemers.org/srfi-145) and
[(scheme bytevector)](http://www.r6rs.org/final/html/r6rs-lib/r6rs-lib-Z-H-3.html#node_chap_2)
are optional dependencies.

# Extensions

This implementation provides the following additional procedures for
inspecting error objects raised by some bytestring procedures; namely,
those satisfying `bytestring-error?`:

`(bytestring-error-message `*error-object*`)`

Returns the message (string) encapsulated by *error-object*.

`(bytestring-error-irritants `*error-object*`)`

Returns a list of the irritants encapsulated by *error-object*.

# Acknowledgements

The implementation of base64 encoding and decoding is from
Alex Shinn's [Chibi Scheme](http://synthcode.com/wiki/chibi-scheme).

The implementation of the bytestring comparison functions is heavily
inspired by Olin Shivers's [SRFI 13](https://srfi.schemers.org/srfi-13)
string comparison code.

# Author

Wolfgang Corcoran-Mathe

Email: wcm at sigwinch dot xyzzy minus the zy

# License

This is free software released under the MIT/X license.  See
LICENSE for details.
