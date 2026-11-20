# Printer Preferences (v2.1.0)

**Printer Preferences** preserves and restores your default printer and per-user printing preferences (duplex, paper tray, color/black-and-white, finishing, user codes, etc.) in non-persistent **RDS, AVD, and Citrix environments** using **FSLogix profile containers** or other roaming profiles.

> **Copyright © Joris Gerretsen 2026** — Licensed under the [MIT License](./LICENSE).

---

## Download
Download the latest installer from the **[Releases](https://github.com/JorisGerretsen/PrinterPreferences/releases/latest)** page (`PrinterPreferences_Setup.exe` — English / Nederlands / Deutsch).

---

## How It Works
In non-persistent RDS, AVD, and Citrix environments, network printers are often removed and recreated at logon by Group Policy (GPO) or workspace management tools. Because Windows deletes per-user printer settings when a printer is removed, users lose their default printer and custom preferences (such as duplex printing or paper trays) on every logon.

**Printer Preferences** solves this cleanly inside the user's own session:
1. **At logon (`/restore`):** Starts hidden in the system tray and waits until all GPO/network printers have finished loading (stabilization check, up to 90 seconds).
2. **Restores default printer:** Checks your user-defined priority list (`DefaultPrinterPriority`) and sets the first available printer as your default printer.
3. **Restores printing preferences (`DEVMODE`):** Restores your saved binary `DEVMODE` (including vendor-specific driver settings such as Ricoh, Brother, or Zebra) into `HKCU\Printers\Connections\,,<server>,<printer>\DevMode`, `HKCU\Printers\DevModes2`, and the session spooler cache (`SetPrinter` level 9).
4. **Never creates printers:** It only restores preferences on printers that are already mapped by GPO/Windows in your session. Unavailable printers are skipped.
5. **Saves changes:** Preferences are saved when you click **Save preferences now** (or **Save** for a single printer) and automatically upon logoff.

---

## Security & No Risk
This application is built specifically for enterprise multi-user environments with strict security requirements:
- **Least privilege (no admin rights required to run):** Runs 100% in the user's own session (`PRINTER_ACCESS_USE`). No Windows service, no elevated privileges, and no access to other users' profiles or settings.
- **No network or internet traffic:** Makes zero outbound connections, opens no ports, and sends no telemetry.
- **No driver or printer installation:** Never installs printer drivers and never creates or modifies printer connections (`HKCU\Printers\Connections` is only updated for existing mapped printers).
- **Protected installation directory:** When installed with `/ALLUSERS`, files are placed in `C:\Program Files (x86)\Printer Preferences\`, where standard users only have read/execute permissions.
- **Local profile storage only:** All user data stays strictly within the user's own profile (`%APPDATA%\Printer Preferences\`).

---

## System Requirements & Compatibility
- **Supported environments:** Intended solely for **RDS (Remote Desktop Services)**, **AVD (Azure Virtual Desktop)**, and **Citrix** combined with **FSLogix profile containers** or other **roaming profiles**.
- **Operating system:** Windows 10 / 11, Windows Server 2016 / 2019 / 2022 / 2025 (x64).
- **Requirements:** Microsoft .NET Framework 4.5 or higher (built-in).

---

## Silent All-Users Installation (for administrators)
Install as Administrator for all users on an RDS/Citrix server (e.g., via GPO, Intune, or Golden Image):

```cmd
PrinterPreferences_Setup.exe /ALLUSERS /VERYSILENT /SUPPRESSMSGBOXES /NORESTART
```

With explicit language (optional: `english`, `dutch`, `german`):
```cmd
PrinterPreferences_Setup.exe /ALLUSERS /VERYSILENT /SUPPRESSMSGBOXES /NORESTART /LANG=english
```

- **Install directory:** `C:\Program Files (x86)\Printer Preferences\`
- **Autostart:** `HKLM\Software\Microsoft\Windows\CurrentVersion\Run` -> `"C:\Program Files (x86)\Printer Preferences\PrinterPreferences.exe" /restore`

---

## Documentation
- [User Guide (English)](./README_EN.txt)
- [Gebruikershandleiding (Nederlands)](./README_NL.txt)
- [Benutzerhandbuch (Deutsch)](./README_DE.txt)

---

## License
This project is licensed under the [MIT License](./LICENSE).
