# Onion Omega2 Firmware Build System

This buildsystem for the LEDE Linux distribution has been modified by Onion Corporation to build firmware for the Onion Omega2 and Omega2+

**Onion Corporation is not responsible for any damage to your device caused by using customer firmware or packages not built and released by Onion Corporation.**

## Notes

* Due to incompatibilities with recent kernel updates, building a firmware with the `Ralink APSoC WiFi SoftAP driver` **will cause a kernel panic during boot**
	* This can be fixed by reflashing the Omega's firmware using the Omega's Bootloader and Ethernet Expansion
	* We are working on a new implementation of the WiFi driver, will be arriving in Q3 2017! Stay tuned!

## Additional Reading

* See `CHANGELOG.md` for a listing of the changes for each firmware version and build
* See `DISCLAIMER.md` for Onion's disclaimer regarding this build system

# LEDE Linux Distribution

This is the buildsystem for the LEDE Linux distribution.

Please use "make menuconfig" to choose your preferred
configuration for the toolchain and firmware.

You need to have installed gcc, binutils, bzip2, flex, python, perl, make,
find, grep, diff, unzip, gawk, getopt, subversion, libz-dev and libc headers.

Run "./scripts/feeds update -a" to get all the latest package definitions
defined in feeds.conf / feeds.conf.default respectively
and "./scripts/feeds install -a" to install symlinks of all of them into
package/feeds/.

Use "make menuconfig" to configure your image.

Simply running "make" will build your firmware.
It will download all sources, build the cross-compile toolchain, 
the kernel and all choosen applications.

To build your own firmware you need to have access to a Linux, BSD or MacOSX system
(case-sensitive filesystem required). Cygwin will not be supported because of
the lack of case sensitiveness in the file system.


Sunshine!
	Your LEDE Community
	http://www.lede-project.org


