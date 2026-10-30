# SigmaOS bulk renamer

A Python command-line tool for previewing and applying regular-expression based
bulk file renames. It follows the Linux Mint Bulky workflow with a preview-first
command, deterministic planning, and collision checks before changes are made.

## Usage

```sh
sigma-renamer-bulk preview /path/to/files --pattern '^img_' --replace 'photo-'
sigma-renamer-bulk apply /path/to/files --pattern '^img_' --replace 'photo-'
```

`preview` is non-mutating. `apply` checks planned destination collisions before
renaming. Review the preview before applying a rename to important files.

## Development

Run `make test` to execute the unit tests and `make build` to compile-check the
Python package. Use `make install` with an appropriate `DESTDIR` to stage the
command-line executable.
