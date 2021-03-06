# Bytestrings

This is an implementation of a
[pre-SRFI specification](https://bitbucket.org/cowan/r7rs-wg1-infra/src/default/BytestringsCowan.md)
by John Cowan which provides bytestrings for Scheme.  It should be
portable to any R7RS-small implementation with
[(scheme bytevector)](http://www.r6rs.org/final/html/r6rs-lib/r6rs-lib-Z-H-3.html#node_chap_2),
[SRFI 1/(scheme list)](https://srfi.schemers.org/srfi-1),
[SRFI 151/(scheme bitwise)](https://srfi.schemers.org/srfi-151), and
one of Scheme's string libraries (one of SRFIs 152, 130, or 13).  In
addition, [SRFI 145](https://srfi.schemers.org/srfi-145)
is an optional dependency.

# Extensions

This implementation provides the following additional procedures for
inspecting error objects raised by some bytestring procedures; namely,
those satisfying `bytestring-error?`:

`(bytestring-error-message` *error-object*`)`

Returns the message (string) encapsulated by *error-object*.

`(bytestring-error-irritants` *error-object*`)`

Returns a list of the irritants encapsulated by *error-object*.

# Implementation Notes

`(hex-string->bytevector s)` returns false if `s` cannot be
interepreted as a base 16 number, in the sense of `string->number`.

# Acknowledgements

The implementation of hex-string and base64 encoding and
decoding is from
Alex Shinn's [chibi-scheme](http://synthcode.com/wiki/chibi-scheme).
This code is found in the *hex.scm* and *base64.scm* files, along
with the chibi-scheme license.

The implementation of several functions is heavily
inspired by Olin Shivers's [SRFI 13](https://srfi.schemers.org/srfi-13).

Of course, any misuse of Alex's or Olin's code or ideas is purely my
own.

# Author

Wolfgang Corcoran-Mathe

Email: wcm at sigwinch dot xyzzy minus the zy

# License

This is free software released under the MIT/X license.  See
LICENSE for details.
