# SUMMARY

`emacs-hmac` implements a Hash-Based Message Authentication Code
around Emacs's built-in `secure-hash` function.

# API

- `(hmac ALGORITHM KEY MESSAGE &optional BINARY)`

  `ALGORITHM` is the hash algorithm to use; it must be one of the
  symbols supported by `secure-hash`, that is: `md5`, `sha1`,
  `sha224`, `sha256`, `sha384`, or `sha512`.  `KEY` is the private key
  to sign with, and `MESSAGE` is the message to sign.  `BINARY` is a
  flag which indicates whether to return a binary or hexadecimal
  string.
  
  Note that while `secure-hash` supports passing a buffer object as
  its `MESSAGE` argument, `hmac` does not.
