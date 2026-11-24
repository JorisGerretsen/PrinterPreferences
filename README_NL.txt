Printer Preferences - Handleiding
=================================

Met dit programma bewaart u uw standaardprinter en afdrukvoorkeuren
(bijvoorbeeld dubbelzijdig of papierlade). Uw voorkeuren worden opgeslagen in
uw gebruikersprofiel en zijn daardoor in elke sessie en op elke server
beschikbaar.

Wijzigingen worden ook automatisch opgeslagen wanneer u zich afmeldt.


Het venster
-----------
Open het venster via het printericoon rechtsonder in het systeemvak.

- Standaardprinter (links)
  Toont uw voorkeurslijst voor de standaardprinter.
  * Verwijderen uit lijst... : haalt de geselecteerde regel uit deze lijst.
  * ↑ / ↓                    : wijzigt de prioriteitsvolgorde van de lijst.

- Beschikbare printers (rechts)
  Toont alle printers die nu in uw sessie beschikbaar zijn. Netwerkprinters
  worden weergegeven als "<printernaam> op <printserver>".
  * Als standaardprinter instellen... : maakt de geselecteerde printer direct
    uw standaardprinter en voegt deze toe aan uw voorkeurslijst.

- Eigenschappen (onderin)
  Toont informatie over de geselecteerde printer (naam, type, driver, poort,
  opmerking, locatie). Hier hoeft u zelf niets aan te passen.
  * Openen... : opent de Windows-afdrukwachtrij van deze printer.
  * Opslaan   : slaat de afdrukvoorkeuren op van alleen deze printer.

- Knoppen onderaan
  * Voorkeuren nu opslaan : slaat uw standaardprinter en de afdrukvoorkeuren
    van ALLE aanwezige printers in een keer op.
  * Afdrukvoorkeuren...   : opent het Windows-venster Afdrukvoorkeuren
    (duplex, kleur, papierlade) voor de geselecteerde printer.
  * Vernieuwen            : ververst de lijst met beschikbare printers.
  * OK                    : sluit het venster. Het programma blijft actief
    in het systeemvak en uw voorkeuren blijven bewaard.


Afdrukvoorkeuren aanpassen
--------------------------
1. Open het venster via het printericoon rechtsonder in het systeemvak.
2. Selecteer rechts de gewenste printer.
3. Klik onderaan op "Afdrukvoorkeuren...".
4. Pas uw instellingen aan (bijvoorbeeld dubbelzijdig of papierlade) en klik
   op OK.
5. Klik op "Voorkeuren nu opslaan" om uw standaardprinter en de voorkeuren van
   alle printers direct op te slaan.
   Let op: de knop "Opslaan" bij Eigenschappen bewaart alleen de
   voorkeuren van de geselecteerde printer.


Systeemvak-menu
---------------
Klik met de rechtermuisknop op het printericoon naast de klok:

- Printerinstellingen openen : opent het venster.
- Voorkeuren nu opslaan      : slaat uw standaardprinter en de voorkeuren van
                               alle printers direct op.
- Standaardprinter           : snel wisselen van standaardprinter.
- Hulp -> Bekijk logbestand  : opent het logbestand in Kladblok. Stuur dit
                               bestand mee als u contact opneemt met de
                               servicedesk over een probleem.
- Hulp -> Info               : toont de actuele versie en copyrightinformatie.
- Afsluiten                  : sluit het programma volledig af.


Problemen?
----------
- Staat een printer niet in de lijst? Klik op "Vernieuwen".


Voor beheerders
---------------
Bestanden en instellingen in het gebruikersprofiel (bijvoorbeeld FSLogix of
een andere profieloplossing):
- Instellingenbestand : %APPDATA%\Printer Preferences\printer_settings.dat (versleuteld)
- Logbestand          : %APPDATA%\Printer Preferences\printerpref.log
- Register            : HKEY_CURRENT_USER\Software\Printer Preferences
