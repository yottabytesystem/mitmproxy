.. _install:

Installation
============

.. _install-ubuntu:

Installation On Ubuntu
----------------------

Ubuntu comes with Python but we need to install pip, python-dev and several libraries.
This was tested on a fully patched installation of Ubuntu 14.04.

.. code:: bash

   sudo apt-get install python-pip python-dev libffi-dev libssl-dev libxml2-dev libxslt1-dev libjpeg8-dev zlib1g-dev g++
   sudo pip install mitmproxy  # or pip install --user mitmproxy

Once installation is complete you can run :ref:`mitmproxy` or :ref:`mitmdump` from a terminal.

On **Ubuntu 12.04** (and other systems with an outdated version of pip),
you may need to update pip using ``pip install -U pip`` before installing mitmproxy.

Installation From Source (Ubuntu)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you would like to install mitmproxy directly from the master branch on GitHub or would like to
get set up to contribute to the project, install the dependencies as you would for a regular
mitmproxy installation (see :ref:`install-ubuntu`).
Then see the Hacking_ section of the README on GitHub.

.. _install-fedora:

Installation On Fedora
----------------------

Fedora comes with Python but we need to install pip, python-dev and several libraries.
This was tested on a fully patched installation of Fedora 23.

.. code:: bash

   sudo dnf install -y python-pip python-devel libffi-devel openssl-devel libxml2-devel libxslt-devel libpng-devel libjpeg-devel
   sudo pip install mitmproxy  # or pip install --user mitmproxy

Once installation is complete you can run :ref:`mitmproxy` or :ref:`mitmdump` from a terminal.


.. _install-arch:

Installation On Arch Linux
--------------------------

mitmproxy has been added into the [community] repository. Use pacman to install it:

>>> sudo pacman -S mitmproxy



Installation On Mac OS X
------------------------

The easiest way to get up and running on OSX is to download the pre-built binary packages from
`mitmproxy.org`_.

There are a few bits of customization you might want to do to make mitmproxy comfortable to use on
OSX. The default color scheme is optimized for a dark background terminal, but you can select a
palette for a light terminal background with the ``--palette`` option.
You can use the OSX **open** program to create a simple and effective ``~/.mailcap`` file to view
request and response bodies:

.. code-block:: none

    application/*; /usr/bin/open -Wn %s
    audio/*; /usr/bin/open -Wn %s
    image/*; /usr/bin/open -Wn %s
    video/*; /usr/bin/open -Wn %s

Once installation is complete you can run :ref:`mitmproxy` or :ref:`mitmdump` from a terminal.


Installation From Source (Mac OS X)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you would like to install mitmproxy directly from the master branch on GitHub or would like to
get set up to contribute to the project, there are a few OS X specific things to keep in mind.

- Make sure that XCode is installed from the App Store, and that the command-line tools have been
  downloaded (XCode/Preferences/Downloads).
- If you're running a Python interpreter installed with homebrew (or similar), you may have to
  install some dependencies by hand.

Then see the Hacking_ section of the README on GitHub.

Installation On Windows
-----------------------

.. note::
    Please note that mitmdump is the only component of mitmproxy that is supported on Windows at
    the moment.

    **There is no interactive user interface on Windows.**


First, install the latest version of Python 3.5 from the `Python website`_.
If you already have an older version of Python 3.5 installed, make sure to install pip_
(pip is included in Python by default). If pip aborts with an error, make sure you are using the current version of pip.

>>> python -m pip install --upgrade pip

Next, add Python and the Python Scripts directory to your **PATH** variable.
You can do this easily by running the following in powershell:

>>> [Environment]::SetEnvironmentVariable("Path", "$env:Path;C:\Python27;C:\Python27\Scripts", "User")

Now, you can install mitmproxy by running

>>> pip install mitmproxy

Once the installation is complete, you can run :ref:`mitmdump` from a command prompt.

Installation From Source (Windows)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you would like to install mitmproxy directly from the master branch on GitHub or would like to
get set up to contribute to the project, install Python as outlined above, then see the
Hacking_ section of the README on GitHub.


.. _Hacking: https://github.com/mitmproxy/mitmproxy/blob/master/README.rst#hacking
.. _mitmproxy.org: https://mitmproxy.org/
.. _`Python website`: https://www.python.org/downloads/windows/
.. _pip: https://pip.pypa.io/en/latest/installing.html
