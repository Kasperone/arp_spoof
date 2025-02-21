# ARP Spoof

This is a Python script that demonstrates ARP spoofing to intercept and manipulate network traffic between a target and a gateway. It is intended for educational purposes to understand ARP poisoning and its implications for network security.

## Features
- Sends spoofed ARP packets to impersonate a gateway or target.
- Intercepts network traffic between the target and gateway.
- Includes functionality to restore ARP tables upon exiting the script.

## Prerequisites
- Python 3.x
- Linux-based operating system
- `scapy` library (for handling ARP packets)

## Installation

Clone the repository to your local machine:

```bash
git clone https://github.com/Kasperone/arp_spoof.git
cd arp_spoofer
```

Install the required library:

```bash
pip install scapy
```

## Usage

Run the script with superuser privileges to perform ARP spoofing.

```bash
sudo python3 arp_spoofer.py
```

### Notes:
- Replace `target_ip` and `gateway_ip` in the script with the IP addresses of the target device and gateway (router), respectively.
- This script sends spoofed ARP packets every 2 seconds to maintain the attack.

### Restoring ARP Tables:
The script includes a cleanup process to restore ARP tables when it is stopped using `CTRL + C`. Ensure you let the script finish properly to avoid disrupting the network.

## Example:

Run the script with the following configuration:

```python
target_ip = "192.168.1.10"
gateway_ip = "192.168.1.1"
```

Output:

```
[+] Packets sent:2
[+] Packets sent:4
[+] Packets sent:6
...
[-] Detected CTRL + C ... Resetting ARP tables.... Please wait.
```

## Notes:
- This script is for educational purposes only. Use it responsibly and only in environments where you have permission to perform testing.
- ARP spoofing is illegal and unethical if performed without authorization.

## Troubleshooting:
- Ensure you have the required libraries installed.
- Verify that you are targeting the correct IP addresses for the gateway and target device.
- Run the script with `sudo` or as root to access network packets.

## License
This project is licensed under the MIT License.

## About

This script is part of the course [Learn Python & Ethical Hacking from Scratch](https://www.udemy.com/course/learn-python-and-ethical-hacking-from-scratch/) on Udemy. The course covers Python scripting and its application in ethical hacking, network security, and more.
