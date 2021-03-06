# asserts-tool

## Install

Install a local copy in an empty directory.

```
GOPATH=`pwd` go get -v github.com/emgee/asserts-tool
```

Run as

```
./bin/asserts-tool ...
```


## Overview

```
Usage:
  asserts-tool [OPTIONS] <command>

Help Options:
  -h, --help  Show this help message

Available commands:
  assertion  generate new assertion
  check      check assertion chain
  key        generate new key
  key-info   inspect signing key
```


## Generate a signing key

```
Usage:
  asserts-tool [OPTIONS] key [key-OPTIONS]

Generate new key that can be used to sign assertions.

Help Options:
  -h, --help         Show this help message

[key command options]
      -n, --name=    Key name (default: Developer)
      -c, --comment= Key comment (default: Generated by asserts-tool)
      -e, --email=   Key email (default: developer@local)
```


## Inspect a signing key

```
Usage:
  asserts-tool [OPTIONS] key-info [file-name]

Inspect a signing key and display the key ID, fingerprint, and encoded public key (as needed for an account-key assertion).

Help Options:
  -h, --help           Show this help message
```


## Generate an assertion

```
Usage:
  asserts-tool [OPTIONS] assertion [assertion-OPTIONS] [file-name]

Generate an assertion, signed by the assertion's authority-id.

Help Options:
  -h, --help             Show this help message

[assertion command options]
      -s, --signing-key= signing key
```


## Verify assertion chain

```
Usage:
  asserts-tool [OPTIONS] check [check-OPTIONS] [file-name...]

Check chain of assertions can be loaded.

Help Options:
  -h, --help             Show this help message

[check command options]
      -t, --trusted-key= trusted key
```
