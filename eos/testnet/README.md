# Testnet script for eos

## Install

First, Install Python3, then install numpy by pip3.

## Boot Testnet

### 1. use eosio build by source

support eosio source at  /path/to/eos, and eosio.contract source at /path/to/contract

use `--root` and `--contracts-dir` param:

```bash
./bios-boot-testnet.py --root /path/to/eos --contracts-dir /path/to/contract -a
```

use `eosio_bin_DIR` to select eosio build bin path source:

```bash
export eosio_bin_DIR=/path/to/eos/build/bin/
./bios-boot-testnet.py --contracts-dir /path/to/contract -a
```

### 2. stop testnet

```bash
./bios-boot-testnet.py -k
```

### 3. restart testnet

use `--root` and `--contracts-dir` param:

```bash
./bios-boot-testnet.py --root /path/to/eos --contracts-dir /path/to/contract -P
```

use `eosio_bin_DIR` to select eosio source:

```bash
export eosio_bin_DIR=/path/to/eos
./bios-boot-testnet.py --contracts-dir /path/to/contract -P
```

### add new node to testnet

testnet script will gen config.ini for each node, just make a copy to /nodes/01-producer111a/config/config.ini.
