# SeaBreeze

![github workflow](https://github.com/desy-fsec/libseabreeze/actions/workflows/tests.yml/badge.svg) [![docs](https://img.shields.io/badge/Documentation-webpages-ADD8E6.svg)](https://desy-fsec.github.io/seabreeze/index.html)

C++-Library for Ocean Optics Spectrometer (Open-source cross-platform spectrometer device driver)

Fork from SVN-Repository at https://sourceforge.net/projects/seabreeze/


## Installation

In order to install `libseabreeze`  on a Linux system the following software packages
are requiered

* a C++17 compatiable compiler
* libusb-0.1
* doxygen in order to build the documentation

If all dependencies are available on your
system you can clone this repository and configure the build

```bash
$ git clone https://github.com/desy-fsec/libseabreeze.git
$ cd libseabreeze
$ make
```
