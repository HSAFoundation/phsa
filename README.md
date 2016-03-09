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

phsa currently consists of three software components which can be used
to implement HSA support to a new platform:

* [gccbrig](https://github.com/HSAFoundation/gccbrig) adds HSAIL input to gcc, thus providing BRIG/HSAIL finalization support for processors that have a gcc backend,
* [phsa-runtime](https://github.com/HSAFoundation/phsa-runtime), a quick-and-dirty fork of the [HSA Runtime Reference Source](https://github.com/HSAFoundation/HSA-Runtime-Reference-Source) that can load the binary (ELF with a special metadata section) output from gccbrig and launch threads that load and execute kernels on the host CPU, and
* [phsa-finalizer](https://github.com/HSAFoundation/phsa-finalizer) that implements the finalization API of the HSA runtime which enables calling gccbrig from phsa-runtime. It also implements several HSAIL builtins as functions.

## IRC channel

phsa's IRC channel is in \#phsa (irc.oftc.net)

## Links

* [Portable Computing Language](http://portablecl.org) (pocl), an open portable
  OpenCL implementation with an HSA driver. This can be added on top of phsa for
  OpenCL 1.2/2.0 programming support.
