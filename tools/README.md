# Tools

## Test Script

[test.sh](./test.sh)

A bash script for running language syntax files against a language parser/compiler/interpreter binary and compare expected results of stdout, stderr, and exit code.

```sh
# Run all tests
BIN="path/to/bin" ./test.sh

# Run tests matching pattern
BIN="path/to/bin" ./test.sh PATTERN

# Update all tests expected files (*.out, *.err, and *.exit)
BIN="path/to/bin" ./test.sh --update

# Update  tests matching pattern expected files (*.out, *.err, and *.exit)
BIN="path/to/bin" ./test.sh PATTERN --update
```
