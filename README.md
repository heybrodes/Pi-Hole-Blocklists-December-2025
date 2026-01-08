# Pi-Hole-Blocklists-January-2026
This repository contains the blocklist sources used by my Pi-hole instance. A collection of Pi-hole adlist URLs used for network-wide DNS-level ad, tracker, and malware blocking. These blocklists are extracted directly from a Pi-hole v6 gravity database and are intended for easy import, backup, or sharing between Pi-hole instances.


## 📦 Contents

- One blocklist URL per line
- Compatible with **Pi-hole v6+**
- Safe for backup, migration, and sharing
- Suitable for version control (Git)

---

## 🚫 What’s Not Included

This repository does **not** include:
- Whitelist entries
- Blacklist entries
- Regex filters
- Client, group, or device configuration
- Compiled gravity data

---

## 🚀 Usage

### Import via Pi-hole Web Interface (Recommended)

1. Open the Pi-hole admin interface
2. Navigate to **Adlists**
3. Copy and paste the contents of the blocklist file
4. Click **Save**
5. Run **Update Gravity**

---

### Import via Command Line

```bash
while read url; do
  pihole -a addlist "$url"
done < pihole-blocklists.txt

pihole -g
