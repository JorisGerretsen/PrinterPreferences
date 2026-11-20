Printer Preferences - User Guide
================================

With this program you can save your default printer and printing preferences
(for example duplex printing or paper tray). Your preferences are stored in
your user profile and are therefore available in every session and on every
server.

Changes are also saved automatically when you log off.


The window
----------
Open the window via the printer icon in the bottom-right system tray.

- Default Printer (left)
  Shows your priority list for the default printer.
  * Remove from list... : removes the selected item from this list.
  * ↑ / ↓               : changes the priority order of the list.

- Available Printers (right)
  Shows all printers currently available in your session. Network printers
  are displayed as "<printer name> on <print server>".
  * Set as default printer... : immediately sets the selected printer as your
    default printer and adds it to your priority list.

- Properties (bottom)
  Displays information about the selected printer (name, type, driver, port,
  comment, location). You do not need to change anything here.
  * Open... : opens the Windows print queue for this printer.
  * Save    : saves the printing preferences for this printer only.

- Bottom buttons
  * Save preferences now    : saves your default printer and the printing
    preferences of ALL available printers at once.
  * Printing preferences... : opens the Windows Printing Preferences window
    (duplex, color, paper tray) for the selected printer.
  * Refresh                 : refreshes the list of available printers.
  * OK                      : closes the window. The program remains active
    in the system tray and your preferences remain saved.


Adjusting printing preferences
------------------------------
1. Open the window via the printer icon in the bottom-right system tray.
2. Select the desired printer on the right.
3. Click "Printing preferences..." at the bottom.
4. Adjust your settings (for example duplex or paper tray) and click OK.
5. Click "Save preferences now" to save your default printer and the
   preferences of all printers immediately.
   Note: the "Save" button under Properties only saves the preferences of
   the selected printer.


System tray menu
----------------
Right-click the printer icon next to the clock:

- Open printer settings : opens the window.
- Save preferences now  : saves your default printer and all preferences
                          immediately.
- Default printer       : quickly switch your default printer.
- Help -> View log file : opens the log file in Notepad. Include this file
                          when contacting the service desk about an issue.
- Help -> About         : shows the current version and copyright information.
- Exit                  : closes the program completely.


Troubleshooting
---------------
- Is a printer missing from the list? Click "Refresh".


For administrators
------------------
Files and settings in the user profile (for example FSLogix or another
profile solution):
- Settings file : %APPDATA%\Printer Preferences\printer_settings.json
- Log file      : %APPDATA%\Printer Preferences\printerpref.log
- Registry      : HKEY_CURRENT_USER\Software\Printer Preferences
