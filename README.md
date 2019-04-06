# Przetak: fewer weeds on the Web

Przetak is a library for checking whether a text contains
abusive or vulgar speech in Polish. While it is written in Go,
it can be used by programs written in many other languages
thanks to FFI (Foreign Function Interface).

## Installation

First, get the package:

```
$ go get github.com/mciura/przetak
```

Change directory to your `${GOPATH}/src/github.com/mciura/przetak`
and run `make` to build the shared library. Depending on your
operating system, the shared library will be called:

* `libprzetak.so` on Linux,
* `libprzetak.dylib` on macOS,
* `przetak.dll` on Windows.

## Usage

Przetak's `evaluate()` function returns an integer whose
bits with respective values 1, 2, or 4 are set if the input
UTF-8 string contains:

* abusive words, e.g. _oszołom_,
* vulgar words with negative connotations, e.g. _ku**a_,
* vulgar words with positive connotations, e.g. _za**bisty_.

The [examples](examples)
directory showcases the use of Przetak directly from Go
and from several other programming languages via FFI
(Foreign Function Interface).

## Author

Marcin Ciura < mciura at gmail dot com >

## License

Przetak is licensed under
[Apache License, Version 2.0](LICENSE).
