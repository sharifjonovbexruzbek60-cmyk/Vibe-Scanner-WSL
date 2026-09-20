# Vibe Scanner WSL

> A defensive network-discovery and TCP port-scanning toolkit for authorized lab environments on Ubuntu WSL.

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Platform](https://img.shields.io/badge/platform-Ubuntu%20WSL-E95420?logo=ubuntu&logoColor=white)](https://learn.microsoft.com/windows/wsl/)
[![Authorized use](https://img.shields.io/badge/use-authorized%20labs-2F6FEB)](#-responsible-use)

## Overview

Vibe Scanner WSL is a learning-focused security toolkit for understanding host discovery, TCP ports, DNS resolution, timeouts, and audit logging in a controlled environment.

## Features

- TCP port discovery with configurable timeouts.
- Local-network discovery using ARP/Scapy where WSL supports it.
- DNS-resolution error handling.
- Scan-result logging for repeatable lab analysis.
- Ubuntu WSL-oriented workflow.

## Requirements

- Ubuntu on WSL
- Python 3.10+
- `scapy` and `colorama` for the corresponding modules
- Administrator privileges only when required by local ARP discovery

## Usage

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python3 daho_scanner.py
```

For local ARP discovery:

```bash
sudo .venv/bin/python network_mapper.py
```

If your checkout uses different entry-point names, run the Python file documented in the source tree.

## WSL notes

ARP discovery can be limited by the WSL networking mode. Prefer testing inside a private lab subnet and keep generated logs out of version control.

## Responsible use

Use this project only against `localhost`, your own lab, or systems for which you have explicit written authorization. Do not scan public infrastructure, evade controls, or disrupt services.

## Roadmap

- Add automated tests for parsing and reporting.
- Add bounded concurrency with safe defaults.
- Add JSON/CSV export.
- Add clearer CLI arguments and validation.

## Author

Behruzbek Sharifjonov — cybersecurity learner and responsible security researcher.
