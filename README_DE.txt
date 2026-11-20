Printer Preferences - Benutzerhandbuch
======================================

Mit diesem Programm speichern Sie Ihren Standarddrucker und Ihre
Druckeinstellungen (zum Beispiel Duplexdruck oder Papierfach). Ihre
Einstellungen werden in Ihrem Benutzerprofil gespeichert und stehen somit in
jeder Sitzung und auf jedem Server zur Verfügung.

Änderungen werden auch automatisch beim Abmelden gespeichert.


Das Fenster
-----------
Öffnen Sie das Fenster über das Druckersymbol unten rechts im Infobereich.

- Standarddrucker (links)
  Zeigt Ihre Prioritätsliste für den Standarddrucker.
  * Aus Liste entfernen... : entfernt den ausgewählten Eintrag aus der Liste.
  * ↑ / ↓                  : ändert die Prioritätsreihenfolge der Liste.

- Verfügbare Drucker (rechts)
  Zeigt alle derzeit in Ihrer Sitzung verfügbaren Drucker an. Netzwerkdrucker
  werden als "<Druckername> auf <Druckserver>" angezeigt.
  * Als Standarddrucker festlegen... : legt den ausgewählten Drucker direkt
    als Standarddrucker fest und fügt ihn Ihrer Prioritätsliste hinzu.

- Eigenschaften (unten)
  Zeigt Informationen zum ausgewählten Drucker an (Name, Typ, Treiber,
  Anschluss, Kommentar, Standort). Hier müssen Sie nichts ändern.
  * Öffnen... : öffnet die Windows-Druckerwarteschlange dieses Druckers.
  * Speichern : speichert die Druckeinstellungen nur für diesen Drucker.

- Untere Schaltflächen
  * Einstellungen jetzt speichern : speichert Ihren Standarddrucker und die
    Druckeinstellungen ALLER verfügbaren Drucker auf einmal.
  * Druckeinstellungen...         : öffnet das Windows-Fenster
    Druckeinstellungen (Duplex, Farbe, Papierfach) für den gewählten Drucker.
  * Aktualisieren                 : aktualisiert die Liste der verfügbaren Drucker.
  * OK                            : schließt das Fenster. Das Programm bleibt
    im Infobereich aktiv und Ihre Einstellungen bleiben erhalten.


Druckeinstellungen anpassen
---------------------------
1. Öffnen Sie das Fenster über das Druckersymbol unten rechts im Infobereich.
2. Wählen Sie rechts den gewünschten Drucker aus.
3. Klicken Sie unten auf "Druckeinstellungen...".
4. Passen Sie Ihre Einstellungen an (z. B. Duplex oder Papierfach) und
   klicken Sie auf OK.
5. Klicken Sie auf "Einstellungen jetzt speichern", um Ihren Standarddrucker
   und die Einstellungen aller Drucker sofort zu speichern.
   Hinweis: Die Schaltfläche "Speichern" unter Eigenschaften speichert nur
   die Einstellungen des ausgewählten Druckers.


Infobereich-Menü
----------------
Klicken Sie mit der rechten Maustaste auf das Druckersymbol neben der Uhr:

- Druckereinstellungen öffnen      : öffnet das Fenster.
- Einstellungen jetzt speichern    : speichert Standarddrucker und alle
                                     Einstellungen sofort.
- Standarddrucker                  : schneller Wechsel des Standarddruckers.
- Hilfe -> Protokolldatei anzeigen : öffnet die Protokolldatei im Editor.
                                     Senden Sie diese Datei mit, wenn Sie
                                     den Service Desk kontaktieren.
- Hilfe -> Info                    : zeigt die aktuelle Version und
                                     Copyright-Informationen an.
- Beenden                          : beendet das Programm vollständig.


Probleme?
---------
- Fehlt ein Drucker in der Liste? Klicken Sie auf "Aktualisieren".


Für Administratoren
-------------------
Dateien und Einstellungen im Benutzerprofil (z. B. FSLogix oder eine andere
Profillösung):
- Einstellungsdatei : %APPDATA%\Printer Preferences\printer_settings.json
- Protokolldatei    : %APPDATA%\Printer Preferences\printerpref.log
- Registrierung     : HKEY_CURRENT_USER\Software\Printer Preferences
