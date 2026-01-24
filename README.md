# covdbg Quick Start

Welcome to [covdbg](https://covdbg.com/)! This guide will help you get started with installing and using covdbg for code coverage analysis on Windows.

## Prerequisites

* Windows 10 (x64) or Windows 11
* PDB files for your native applications (required for symbol resolution)
* A covdbg license (via `COVDBG_LICENSE` or `COVDBG_LICENSE_FILE` environment variable)
* covdbg installed (see Installation section below)

## Installation

Follow the [Installation Guide](https://covdbg.com/docs/getting-started/installation/) to set up covdbg on your system. You can choose between the MSI installer for a machine-wide installation or a portable ZIP archive for a flexible setup.

## Build

Ensure your native application is built with debug symbols (PDB files). This is essential for covdbg to map executed code back to source lines.

For this example, we will use a sample application called `app.exe` with its corresponding `app.pdb`.

To build the example application using Visual Studio:

1. Configure the project with CMake. `cmake -S . -B build`
2. Build the project. `cmake --build build --config Debug`

After this is done you should have `app.exe` and `app.pdb` in the `build/Debug` directory.
