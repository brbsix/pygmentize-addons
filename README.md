# pygmentize-addons

`pygmentize-addons` consists of two scripts to make use of Pygment's handy pygmentize program. The scripts are used for rapid inspection of syntax highlighted source code. `pygshit` is for use from the terminal and `pygsparkle` is used for GUI use.

Installation
------------

To install on Linux systems:

    sudo install pygshit pygsparkle /usr/local/bin
    sudo install -m 0644 pyg-completion /etc/bash_completion.d/pyg

Requirements
------------

`pygmentize-addons` requires pygmentize which is part of Pygments. Most people will want to install this via their distribution's package manager. It is also available via pip (package manager for Python).

To install Pygments to your system:

    sudo apt-get install python-pygments

To install Pygments to your local bin folder via pip:

    pip install --user Pygments

*Note: pygsparkle requires an image viewer capable of viewing PNG images. It is currently configured to use ristretto (default image viewer on XFCE) but feel free to change it. It is stored in the VIEWER variable near the top of the file.*

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

`pygsparkle` is used to display PNG images of syntax highlighted code. It is used the same as `pygshit`, lacking only the '-l/--less' option.

License
-------

Copyright (c) 2015 Six (brbsix@gmail.com).

Licensed under the GPLv3 license.
