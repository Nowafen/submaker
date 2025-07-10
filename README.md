# Submaker

**Submaker** is a simple yet powerful Bash-based utility designed to generate custom wordlists for DNS brute-forcing. It leverages `assetfinder` to extract subdomains for given domains and processes them to create a clean, de-duplicated wordlist of subdomain patterns that can later be used in enumeration or fuzzing phases during reconnaissance.

> 🧠 Although this repo hosts the **open-source** version of the script for educational purposes, the main release is closed-source to protect from code plagiarism.

---

## 🔥 Why Use Submaker?

- Helps in crafting **target-specific wordlists** for DNS brute-force attacks.
- Extracts subdomain structures from real assets found via `assetfinder`.
- Highly useful in **bug bounty**, **penetration testing**, and **attack surface mapping**.
- Lightweight, fast, and written in pure Bash.

---

## ⚙️ Features

- Auto version checking and update support
- Input/output file support
- Cleans and formats raw subdomains into reusable wordlists
- Progress bar and subdomain stats
- Error handling and colored output

---

## 🛠️ Installation

1. Clone the repo:
   ```bash
   git clone https://github.com/Nowafen/submaker.git
   cd submaker
   ```

2. Make the script executable:
   ```bash
   chmod +x submaker.sh
   ```

3. Install [assetfinder](https://github.com/tomnomnom/assetfinder) if not already installed:
   ```bash
   go install github.com/tomnomnom/assetfinder@latest
   export PATH=$PATH:$(go env GOPATH)/bin
   ```

---

## 🚀 Usage

```bash
./submaker.sh -f domains.txt -o wordlist.txt
```

### Options:

| Option         | Description                                                |
|----------------|------------------------------------------------------------|
| `-f, --file`   | Path to input file containing domains (one per line)       |
| `-o, --output` | Output wordlist file (default: `wordlist.txt`)             |
| `-up`          | Check for updates and auto-update                          |
| `-h`           | Display help and usage instructions                        |

---

## 📌 Example

```bash
./submaker.sh -f targets.txt -o subdomains-wordlist.txt
```

This will:
- Fetch subdomains of all domains in `targets.txt`
- Extract subdomain structures
- Save them as a clean wordlist in `subdomains-wordlist.txt`

---

## ⚠️ Notes

- You **must** have `assetfinder` installed and accessible in your `$PATH`.
- Output file **must** have a `.txt` extension.
- Make sure your input file doesn’t have empty lines.

---

## 🧪 Version

Current: **v1.1**

---

## 📁 Repository

[https://github.com/Nowafen/submaker](https://github.com/Nowafen/submaker)

