# RSA Factoring Challenge

This project explores how weak RSA key generation can make it possible to
recover factors of a public modulus. It contains small Python experiments for
factoring integers and is intended for learning about integer factorization
and public-key cryptography.

## Project contents

There are no nested task directories in the repository at present. Both task
scripts are in the repository root:

| Task | File | Description |
| --- | --- | --- |
| Difference-of-squares factorization | [`factors`](./factors) | A Fermat-style search for factors using a difference of two squares. |
| Pollard p-1 factorization | [`rsa`](./rsa) | An attempted Pollard p-1 factorization flow with a primality-checking step. |

## Requirements

- Python 3
- No third-party packages are currently required.

The original project brief specified Ubuntu 20.04 LTS. The scripts use the
Python standard library, but have not been verified across operating systems.

## Input and intended use

Both scripts are designed to receive a text-file path as their command-line
argument. The `factors` task is intended to process integers listed in the
file, while `rsa` currently reads the first integer only. The input format is
one integer per line.

These scripts are work in progress and are **not currently runnable**: both
fail Python's syntax check. Check and fix the scripts before attempting to run
them:

```sh
python3 -m py_compile factors rsa
```

Once repaired, their intended command-line interface is:

```sh
./factors path/to/numbers.txt
./rsa path/to/numbers.txt
```

## Repository hygiene

The [`.gitignore`](./.gitignore) excludes generated Python files, local virtual
environments, Node dependency directories, and common local database files.
Do not commit generated dependencies or local database data.
