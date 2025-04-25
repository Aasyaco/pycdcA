# pycdc

[![C/C++ CI](https://github.com/zrsx/pycdc/actions/workflows/c-cpp.yml/badge.svg)](https://github.com/zrsx/pycdc/actions/workflows/c-cpp.yml)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-linux%20%7C%20termux-lightgrey)]()
[![Forked from zrax/pycdc](https://img.shields.io/badge/forked%20from-zrax%2Fpycdc-blue)](https://github.com/zrax/pycdc)

**pycdc** is a fast, lightweight Python bytecode decompiler developed and maintained by the [zrsx](https://github.com/zrsx) organization. It converts `.pyc` files—compiled Python bytecode—back into readable Python source code.

This fork includes performance optimizations, codebase cleanups, and broader compatibility with newer Python versions.

---

## Features

- Decompiles `.pyc` files from CPython
- Minimal dependencies — C++ only
- Cross-platform (Linux, Termux, macOS, Windows via WSL)
- Easy CLI usage

---

## Installation

### One-Line Installer (Linux & Termux)

```bash
bash <(curl -s https://raw.githubusercontent.com/zrsx/pycdc/main/install.sh)
```

> Note: Ensure you have `curl`, `git`, `cmake`, and a C++ compiler (`g++` or `clang`) installed.

---

## Manual Build Instructions

### Prerequisites

Install the following packages:

#### Debian / Ubuntu

```bash
sudo apt update
sudo apt install -y git cmake build-essential
```

#### Termux (Android)

```bash
pkg update
pkg install git cmake clang make
```

---

### Build Steps

```bash
# Clone the repository
git clone https://github.com/zrsx/pycdc.git
cd pycdc

# Create and navigate into the build directory
mkdir build && cd build

# Configure and build
cmake ..
make -j$(nproc)
```

The `pycdc` binary will be available in the `build/` directory.

---

## Usage

```bash
./pycdc <path_to_file.pyc>
```

Example:

```bash
./pycdc __pycache__/example.cpython-312.pyc
```

Output will be printed directly to the terminal.

---

## GitHub Actions (CI/CD)

The project uses GitHub Actions to automate builds on every push and pull request:


---

## License

This project is licensed under the [MIT License](LICENSE), in accordance with the original [zrax/pycdc](https://github.com/zrax/pycdc) repository.

---

## Credits

- Original author: [zrax](https://github.com/zrax/pycdc)
- Maintained and enhanced by: [zrsx Organization](https://github.com/zrsx)
- 
