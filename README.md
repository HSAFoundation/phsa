# Portable HSA (PHSA)

PHSA is a project aiming to implement the Heterogeneous System Architecture
standard's software parts (PRM and the runtime). The goal is a high performance HSA implementation which is portable to
a variety of platforms. The supported Kernel agents also include non-GPU-style
processors such as CPUs and DSPs.

This repository includes instructions for adapting and using the multiple
software components that together form phsa.

**Please note that PHSA is an unfinished in progress project and not
yet suitable for wide spread use.** If you want to participate in the development,
take a look at the TODOs in each of the components as listed below.

## Components

phsa currently consists of two software components which can be used
to implement HSA support to a new platform:

* [gccbrig](https://github.com/HSAFoundation/gccbrig) adds HSAIL input to gcc, thus providing BRIG/HSAIL finalization support for processors that have a gcc backend,
* [phsa-runtime](https://github.com/HSAFoundation/phsa-runtime), generic implementation of HSA Runtime Specification 1.0. It is designed to be used with the GCC's BRIG frontend for finalization support.

## IRC channel

phsa's IRC channel is in \#phsa (irc.oftc.net)

## Links

* [Portable Computing Language](http://portablecl.org) (pocl), an open portable
  OpenCL implementation with an HSA driver. This can be added on top of phsa for
  OpenCL 1.2/2.0 programming support.
