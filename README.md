# pygmentize-addons

`pygmentize-addons` consists of two scripts to make use of the Python Pygment library for rapid inspection of syntax highlighted source code. `pygshit` is for terminal use and `pygsparkle` is for GUI use.

Installation
------------

To install on Linux:

    sudo install pygshit pygsparkle /usr/local/bin
    sudo install -m 0644 pyg-completion /etc/bash_completion.d/pyg

Requirements
------------

`pygmentize-addons` requires Pygments. It is compatible with the version for Python 2 (python-pygments) in addition to the version for Python 3 (python3-pygments). Most people will want to install Pygments via their distribution's package manager. It is also available via pip (the Python package manager).

To install Pygments to your system:

    sudo apt-get install python-pygments

To install Pygments to your local bin folder via pip:

    pip install --user Pygments

*Note: `pygsparkle` requires an image viewer capable of viewing PNG images. It is currently configured to use ristretto (the default image viewer in XFCE) but feel free to change it. The value is stored in the VIEWER variable near the top of the file.*

Usage
-----

`pygshit` is used to display syntax highlighted code in the terminal.

To display code:

    pygshit ./script.sh

To display code via `less`:

    pygshit -l ./script.sh

To display code for an installed script (on the PATH):

    pygshit -x script

To display code for an installed script (on the PATH) via `less`:

    pygshit -lx script

`pygsparkle` is used to display PNG images of syntax highlighted code. It is used the same as `pygshit`, lacking only the `-l/--less` option.

License
-------

Copyright (c) 2015 Six (brbsix@gmail.com).

Licensed under the GPLv3 license.
