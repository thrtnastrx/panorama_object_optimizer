# panorama_object_optimizer
De-duplicates shared objects in Panorama, and provides either an optimized XML or a full set of "set" commands to de-duplicate objects and replace the objects wherever they appear in policies.
# Panorama Object Optimizer

### Offline Duplicate Object Consolidation & CLI Export Tool for Palo Alto Panorama

This GUI-based Python application helps engineers identify and consolidate **duplicate address objects** from exported Panorama XML configurations.  

> 🆕 **"Export CLI Commands"** — generates Panorama‐ready `set` / `delete` commands that:
> - Create merged shared objects.
> - Update **Security Policy** references (source/destination).
> - Remove the old duplicate objects.

---

## 🚀 Features

- ✅ **Offline operation** — works entirely from Panorama XML exports, no API key needed.
- ✅ **Duplicate detection** — identifies identical IP/FQDN address objects.
- ✅ **Automatic merge naming** — supports optional prefix, suffix, and "set name to value" modes.
- ✅ **Safe XML editing** — merges objects into the shared config section.
- ✅ **CLI export** — generates command-line equivalents for Panorama commit-safe execution.
- ✅ **Reference updates** — security policy rules referencing old objects are updated automatically.
- ✅ **Mac-native GUI** — built with `tkinter`, tested on macOS Sonoma (Apple Silicon).

---

## 🧰 Requirements

| Dependency | Purpose | Version |
|-------------|----------|----------|
| Python | Core language | ≥ 3.11 |
| tkinter | GUI framework | (built-in) |
| xml.etree.ElementTree | XML parser | (built-in) |
| collections | Data structure utilities | (built-in) |
| datetime | Timestamps | (built-in) |
| os | File management | (built-in) |

### Optional install via pip

Create your project directory:
```bash
mkdir -p /Users/206788335/py/pan_objects
cd /Users/206788335/py/pan_objects
