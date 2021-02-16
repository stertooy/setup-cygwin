# setup-cygwin-for-gap

This GitHub action downloads and prepares an instance of cygwin for the use
with GAP.

## Usage

By default it downloads and installs cygwin and downloads packages needed to
compile and run GAP.

Its behaviour can be customized via the inputs below.

### Inputs

All of the following inputs are optional.

- `PKGS_TO_INSTALL`:
    - The packages to install
    - default: `'wget,git,gcc,gcc-g++,gcc-core,m4,libgmp-devel,make,automake,libtool,autoconf,autoconf2.5,zlib-devel,libreadline-devel'`

## Contact
Please submit bug reports, suggestions for improvements and patches via
the [issue tracker](https://github.com/gap-actions/setup-cygwin-for-gap/issues)
or via email to
[Sergio Siccha](mailto:siccha@mathematik.uni-kl.de).

## License
The action `setup-cygwin-for-gap` is free software; you can redistribute
and/or modify it under the terms of the GNU General Public License as published
by the Free Software Foundation; either version 2 of the License, or (at your
opinion) any later version. For details, see the file `LICENSE` distributed
with this action or the FSF's own site.
