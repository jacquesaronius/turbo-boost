# Turbo — Simple Intel Turbo Boost Toggle Script

`turbo` is a lightweight Bash utility that allows you to toggle **Intel Turbo Boost** on or off from the command line. It also provides a **status** mode so you can quickly check whether Turbo Boost is currently enabled.

This script works by interacting with the kernel’s Turbo Boost control interface:

```
/sys/devices/system/cpu/intel_pstate/no_turbo
```

A value of:

- **0** → Turbo Boost **Enabled**
- **1** → Turbo Boost **Disabled**

---

## Features

- Toggle Turbo Boost on/off with a single command  
- Check current Turbo Boost status  
- Simple, fast, no dependencies  
- Works on systems using the `intel_pstate` driver

---

## Usage

### Check Turbo Boost Status

```
turbo status
```

Output will be either:

- `TurboBoost is currently Enabled`
- `TurboBoost is currently Disabled`

---

### Toggle Turbo Boost

Just run:

```
turbo
```

If Turbo Boost is enabled, it will be disabled.  
If Turbo Boost is disabled, it will be enabled.

---

### Invalid Arguments

If you pass anything other than `status`, the script will warn you:

```
<argument> is not a valid argument.
```

---

## Installation

Save the script as `turbo`.

Make it executable:

```
chmod +x turbo
```

Copy it into `/usr/local/bin` so it’s available system‑wide:

```
sudo cp turbo /usr/local/bin/
```

Test it:

```
turbo status
```

---

## Requirements

- Linux system using the `intel_pstate` CPU driver  
- Root privileges to modify:

