# PHP CGI Argument Injection Detector (CVE-2024-4577) murrezsec x carsxn

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
(+) Potential vulnerability detected at: https://example.com/cgi-bin/php-cgi.exe
(-) No vulnerability detected at: https://example.com/php-cgi/php-cgi.exe
```

---

## Project Structure

```
php-cgi-argument-injection-detector/
│
├── asdqwe.py
├── README.md
└── LICENSE
```

---

## Intended Audience

* Security researchers
* System administrators
* Blue team and defensive security practitioners
* Academic and laboratory environments

---

## Security Policy

### Responsible Use

This repository follows a strict responsible disclosure and usage policy. The code provided here is intended solely for defensive security testing, academic research, and educational demonstrations.

Users are expected to:

* Test only systems they own or have explicit written permission to test
* Avoid any form of unauthorized scanning or probing
* Use the results only to improve system security

Any misuse of this project is a direct violation of this policy.

---

## Disclaimer

This tool is provided for informational purposes only. The author makes no guarantees regarding accuracy, completeness, or effectiveness.

Under no circumstances shall the author be held liable for:

* Direct or indirect damages
* Data loss or service disruption
* Legal consequences arising from improper or illegal use

Use of this software constitutes acceptance of these terms.

---

## License

MIT License

---

## Final Notes

This project references publicly disclosed vulnerability information and is intended to support defensive security efforts.

The author does not endorse or support malicious use of this software under any circumstances.
