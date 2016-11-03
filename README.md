# kodkodi

This repository contains a PKGBUILD for archlinux users who wish to install
[kodkodi](http://people.mpi-inf.mpg.de/~jblanche/). Kodkodi is a frontend for
[kodkod](http://alloy.mit.edu/kodkod/), a constraint solver for relational
first-order logic.

## Use

Well, let's assume you use archlinux. The following commands will
clone this repository, build the package and install it (you might need
`sudo` for the last line, as it requires root privileges)

    $ git clone https://github.com/nunchaku-inria/kodkodi-pkg.git
    $ cd kodkodi-pkg
    $ makepkg
    $ pacman -U kodkodi-2.0-1-any.pkg.tar.xz

Then you can invoke `kodkodi` as a command line tool.
