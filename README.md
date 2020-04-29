# Pascal radio utilities by G4FGQ

[![image](https://travis-ci.org/scivision/radioutils-pascal.svg?branch=master)](https://travis-ci.org/scivision/radioutils-pascal)

These files are preserved on Github in case the
[archived (deceased) author's website](http://www.zerobeat.net/G4FGQ/#S104)
goes down.

Also of interest may be
[Pascal Intermodulation calculator](https://github.com/scivision/intermodulation-calculator/).

[CMake4Pascal](https://github.com/daar/CMake4Pascal)
is credited for the `cmake_modules/` and getting CMake to work with Pascal.

## Prereq

* Linux: `apt install fp-compiler`
* Mac: `brew install fpc`
* [Windows](https://www.freepascal.org/download.var)

## Build

```sh
cmake -B Build
cmake --build build

cd build
ctest -V
```
