# Info4Ports
**Info4Port** is a lightweight Bash-based CLI tool for identifying TCP services by port number. Built for pentesters, red teamers, blue teamers, and sysadmins who need fast offline intelligence on what runs behind common ports.

> 🧠 Designed for speed and clarity. No dependencies. No guessing.

---

## 📦 Features

- 🔎 Instant port-to-service lookup using a local hardcoded dictionary
- 🧠 Optional verbose mode to get descriptive analysis per port
- ⚔️ Fully offline – works in air-gapped environments
- 🐚 Bash-native and easily portable
- 📋 Supports multiple ports at once via comma-separated input

---

## 🚀 Usage

```bash
./Info4Port -p22,80,443
```

```
[+] Port 22 → SSH
[+] Port 80 → HTTP
[+] Port 443 → HTTPS
```

```bash
./Info4Port -p21,3306,445 -i
```

```
[+] Port 21 → FTP – File Transfer Protocol: Transfers files between systems using the TCP protocol.
[+] Port 3306 → MySQL: Popular open-source relational database system used in web applications.
[+] Port 445 → SMB – Server Message Block: Provides shared access to files, printers, and serial ports.
```

---

## 🛠️ Installation

Make it executable:

```bash
chmod +x Info4Port
```

(Optional) Move it to a system-wide location:

```bash
sudo mv Info4Port /usr/local/bin/info4port
```

Use it anywhere:

```bash
info4port -p443
```

---

## ⚙️ Flags

| Flag        | Description                                                       |
|-------------|-------------------------------------------------------------------|
| `-pPORTS`   | Comma-separated list of ports (required). Example: `-p22,80,443`  |
| `-i`        | (Optional) Enable verbose mode to show port descriptions          |

---

## 🧪 Sample Output

```bash
$ ./Info4Port -p53,161,443 -i

[+] Port 53 → DNS – Domain Name System: Resolves domain names to IP addresses.
[+] Port 161 → SNMP – Simple Network Management Protocol: Used for monitoring and managing network devices.
[+] Port 443 → HTTPS – HyperText Transfer Protocol Secure: Encrypted web traffic.
```

---

## 🧑‍💻 Author

**Yi-Kyu**  
Ethical Offensive Security | Red Team Tools | Bash Automation  
[GitHub](https://github.com/Yi-Kyu) • [Portfolio](https://yi-kyu.github.io)

---

## ⚔️ License

This project is open-source and licensed under the [MIT License](LICENSE).
