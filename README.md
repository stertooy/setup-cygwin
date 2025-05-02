# setup-cygwin V2

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
    - default: `'wget,git,gcc-g++,gcc-core,libgmp-devel,make,libtool,autoconf,zlib-devel,libreadline-devel,xdg-utils'`
- `extra-pkgs-to-install`:
    - Comma-separated list containing the extra Cygwin packages needed to install additional packages
    - default: `''`

## Contact
Please submit bug reports, suggestions for improvements and patches via
the [issue tracker](https://github.com/gap-actions/setup-cygwin/issues).

## License
The action `setup-cygwin` is free software; you can redistribute
and/or modify it under the terms of the GNU General Public License as published
by the Free Software Foundation; either version 2 of the License, or (at your
opinion) any later version. For details, see the file `LICENSE` distributed
with this action or the FSF's own site.
