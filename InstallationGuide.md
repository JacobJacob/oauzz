# Introduction #

OAuzz has been developed in Python to be cross-platform; so no real installation is required.

Nevertheless, OAuzz requires external librearies to work. These libraries have to be installed previously.


# Details #

The main libraries which are used by OAuzz are:

  * [PyCrypto - https://www.dlitz.net/software/pycrypto/](https://www.dlitz.net/software/pycrypto/)
  * urllib and urllib2
  * sqlite3
  * BaseHTTPServer, urlparse, getpass, random, math, sys and time

From the above list, the only library has to be installed is PyCrypto. The rest of them are part of the basic Python installation.


### PyCrypto ###

  1. Download PyCrypto from https://www.dlitz.net/software/pycrypto/
  1. Install it (Linux example):
```
# Untar it (x.y must be replaced for the downloaded version)
$ tar zxvf pycrypto-x.y.tar.gz

# Configure it
$ cd pycrypto-x.y/
$ ./configure

# Build it
$ python setup.py build

# Install it
$ sudo python setup.py install
```

**NOTE**: If during the configuration (./configure step) you have any problem related to 'src/MD2.C' file because 'Python.h' file cannot be found:
```
src/MD2.c:31:20: fatal error: Python.h: No such file or directory
```
you have to install python-dev previously:
```
# Install python-dev if you don't have it
$ sudo apt-get install python-dev
```