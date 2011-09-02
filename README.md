# peater: the Archlinux's packages eater.

**peater** (the packages eater) eats [ all | part of ] your installed packages and saves them to a list, or if you 
want it restores all the packages in a list.

## Features

  * save all the installed packages to a list;
  * save a subset of installed packages to a list;
  * restore a list of packages (and optionally execute a script after restore).

## Precondition:

To make the script work correctly you must have installed:

  * bash; 
  * pacman; 
  * packer.

## Installation & Basic Usage:

To install the script, copy it wherever you want. If you run an Archlinux box you can use the included PKGBUILD.

### Save

To save all packages in the system, simply run

    $ peater -sa

or if you want specify a list's name

    $ peater -sa foo.pkglist

To save a subset of the installed packages, run

    $ peater -s foo.pkglist bar baz

and **peater** will save all your installed packages containing the pattern 'bar' and 'baz' in to the list 'foo.pkglist'.

### Restore

To restore the packages inside a list, you have to run
    
    $ peater -r foo.pkglist

and **peater** will restore all the package contained in the list 'foo.pkglist'. If in the directory of  'goo.pkglist', 
there is a file named 'foo.sh', **peater** will execute it after restoring packages.

## Author:

Luca Cesari <mirshann@freakmind.org>

## License:

**peater** is licensed under the terms of the MIT License, see the included LICENSE file.

