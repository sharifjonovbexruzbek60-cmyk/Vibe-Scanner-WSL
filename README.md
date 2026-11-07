# Vibe Scanner WSL

A learning-focused network discovery and TCP port-scanning toolkit for authorized lab environments, developed with Ubuntu on WSL in mind.

The project helps me practice networking concepts such as host discovery, DNS resolution, TCP ports, timeouts, and recording results in a controlled environment.

## Features

- TCP port discovery with configurable timeouts
- Local-network discovery using ARP/Scapy where supported by WSL
- DNS-resolution error handling
- Logging to support repeatable lab analysis

## Requirements

- Ubuntu on WSL
- Python 3.10 or later
- `scapy` and `colorama` for the modules that use them
- Elevated privileges only when required for local ARP discovery

## Getting started

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python3 daho_scanner.py
```

For local ARP discovery, if supported by your WSL networking configuration:

```bash
sudo .venv/bin/python network_mapper.py
```

Check the source tree for the available entry points and requirements. WSL networking modes may limit ARP discovery; use a private lab network and avoid committing generated logs.

## Responsible use

Use this project only on `localhost`, your own lab, or systems for which you have explicit authorization. Do not scan public infrastructure or use the tool to evade controls or disrupt services.

## About

Built by Behruzbek Sharifjonov as part of my ongoing learning in Python, networking, and responsible cybersecurity.
