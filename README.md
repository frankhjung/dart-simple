# Simple Dart CLI Program Example

A sample command-line application providing basic argument parsing with an
entrypoint in `bin/`.

## Compile

Generate a local executable with the following command:

```bash
$ dart compile exe --target-os linux -o bin/simple bin/simple.dart
Generated: /home/frank/dev/dart/simple/bin/simple
```

This generates the following file:

```bash
$ file bin/simple
bin/simple: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 2.6.32, stripped
```

## Run

To run the program, use the following command:

```bash
dart run simple help
```

```bash
$ time dart run simple help version verbose
Building package executable...
Built simple:simple.
Positional arguments: [help, version, verbose]

real 0m1.062s
user 0m1.251s
sys 0m0.151s
```

Compare this to the compiled version:

```bash
$ time bin/simple help version verbose
Positional arguments: [help, version, verbose]

real 0m0.009s
user 0m0.005s
sys 0m0.006s
```

### Examples

```bash
$ dart run simple:simple version
Building package executable...
Built simple:simple.
Positional arguments: [version]
```

```bash
$ dart run simple verbose help version
Building package executable...
Built simple:simple.
Positional arguments: [verbose, help, version]
```

## Testing

TODO: Add unit tests.

## Checks

TODO: Add linting and formatting checks.
