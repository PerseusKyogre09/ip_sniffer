# Port Sniffer CLI

A simple, multi-threaded TCP port scanner written in Rust.

## Overview

This command-line utility allows you to scan an IP address (IPv4 or IPv6) for open TCP ports. It utilizes multi-threading to perform port scanning efficiently.

## Features

- Scan any IPv4 or IPv6 address for open TCP ports
- Configurable number of threads for faster scanning
- Simple command-line interface
- Real-time feedback during scanning
- Sorted output of open ports

## Installation

### Prerequisites

- Rust and Cargo (Install from [rust-lang.org](https://www.rust-lang.org/tools/install))

### Building from source

```bash
git clone https://github.com/yourusername/port-sniffer-cli.git
cd port-sniffer-cli
cargo build --release
```

The compiled binary will be available at `target/release/ip_sniffer`.

## Usage

### Basic usage

Scan an IP address with the default settings (4 threads):

```bash
ip_sniffer 192.168.1.1
```

### Advanced usage

Specify the number of threads to use:

```bash
ip_sniffer -j 10 192.168.1.1
```

### Help

Display the help message:

```bash
ip_sniffer -h
```

## Examples

Scan a local IP address:

```bash
ip_sniffer 127.0.0.1
```

Scan with 16 threads:

```bash
ip_sniffer -j 16 8.8.8.8
```

## Output

The program shows progress during scanning with dots (`.`) and then displays a list of open ports:

```
....
22 is open
80 is open
443 is open
```

## Performance

Performance depends on the number of threads used and network conditions. Increasing the number of threads can improve scanning speed, but may also increase network traffic.

## License

[MIT License](LICENSE)

## Disclaimer

Port scanning may be prohibited by some network providers or organizations. Only use this tool on networks you own or have explicit permission to scan.