# PHP CGI Argument Injection Detector (CVE-2024-4577) murrezsec🕊️/carsxn

This repository contains a Python-based detection script intended to identify potential exposure to **PHP CGI Argument Injection vulnerabilities**, specifically **CVE-2024-4577**.

This project is provided **for informational, educational, and defensive security purposes only**.

---

## Legal Disclaimer

This software is provided "as is", without warranty of any kind, express or implied. The author assumes **no responsibility or liability** for any misuse, damage, or legal consequences resulting from the use of this tool.

By using this software, you agree that:

* You have **explicit authorization** to test the target systems
* You are solely responsible for complying with all applicable laws and regulations
* The author cannot be held liable for any actions performed with this tool

Unauthorized scanning or testing of systems is **strictly prohibited**.

---

## Purpose and Scope

The purpose of this tool is to assist security researchers and system administrators in identifying **potential misconfigurations** related to PHP CGI deployments.

This script:

* Does **not** perform exploitation
* Does **not** attempt to gain unauthorized access
* Does **not** deploy payloads beyond basic detection indicators

It only checks for publicly known exposure patterns associated with CVE-2024-4577.

---

## Vulnerability Background

**CVE-2024-4577** is a PHP CGI Argument Injection vulnerability that may affect improperly configured PHP CGI environments. Under certain conditions, attackers could manipulate PHP interpreter arguments, potentially leading to remote code execution.

This tool merely inspects server responses for signs of possible exposure and should not be considered a comprehensive security assessment.

---

## Requirements

* Python 3.8 or later
* requests library

Installation:

```bash
pip install requests
```

---

## Usage

```bash
python asdqwe.py --target https://example.com
```

Arguments:

* `-t`, `--target`: Target base URL

Sample output:

```
(+) Potential vulnerability detected at: ht
```
