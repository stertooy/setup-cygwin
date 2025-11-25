# setup-cygwin

This GitHub action downloads and prepares an instance of cygwin for the use
with GAP.

## Usage

By default it downloads and installs cygwin and downloads packages needed to
compile and run GAP.

Its behaviour can be customized via the inputs below.

### Inputs

All of the following inputs are optional.

- `pkgs-to-install`:
    - Comma-separated list containing the Cygwin packages needed to install GAP
    - default: `'wget,git,gcc-g++,gcc-core,libgmp-devel,make,libtool,autoconf,zlib-devel,libreadline-devel,xdg-utils,automake'`
- `extra-pkgs-to-install`:
    - Comma-separated list containing the extra Cygwin packages needed to install additional packages
    - default: `''`

### What's new in v2

In v2 most of the implementation of this action has been rewritten. While this
by itself should not cause issues in an ideal world, we can not guarantee this
100%, but we recommend you just try it (and if there is a problem, report the
issue and possibly revert to v1).

Moreover the `EXTRA_PKGS_TO_INSTALL` input was renamed to `extra-pkgs-to-install`,
and `PKGS_TO_INSTALL` was renamed to `pkgs-to-install`.

### Examples

The following is a minimal example to run this action.

```yaml
name: CI

on:
  push:
  pull_request:

jobs:
  # The CI test job
  test:
    name: CI test
    runs-on: windows-latest

    steps:
      - uses: actions/checkout@v6
      - uses: gap-actions/setup-cygwin@v2
      # ... additional steps using GAP will usually follow here
```

## Contact
Please submit bug reports, suggestions for improvements and patches via
the [issue tracker](https://github.com/gap-actions/setup-cygwin/issues).

## License
The action `setup-cygwin` is free software; you can redistribute
and/or modify it under the terms of the GNU General Public License as published
by the Free Software Foundation; either version 2 of the License, or (at your
opinion) any later version. For details, see the file `LICENSE` distributed
with this action or the FSF's own site.
