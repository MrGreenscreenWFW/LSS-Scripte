
# Mission Chief Wachen-Umbenennungsskript

## Übersicht
Dieses JavaScript-Skript wurde entwickelt, um in [Mission Chief](https://www.leitstellenspiel.de) automatisch die Namen von Wachen auf Grundlage von Standort- und Landkreis-Informationen umzubenennen. Dabei wird die OpenStreetMap-Geocoding API verwendet, um die Koordinaten in Standortinformationen zu konvertieren.

## Merkmale
- **Automatische Umbenennung**: Basierend auf dem Standort und dem Landkreis der Wachen werden die Namen automatisch in einem festgelegten Format angepasst.
- **Anpassbares Namensschema**: Das Schema für die neuen Gebäudenamen kann individuell konfiguriert werden.
- **Einheitenerkennung**: Basierend auf dem Gebäudetyp wird die entsprechende BOS-Einheit (z. B. Feuerwehr, Rettungsdienst, Polizei) automatisch zugewiesen.
- **Fortschrittsanzeige**: Im Konsolenfenster wird der Fortschritt der Umbenennung angezeigt.
  
## Installation
1. Öffne die JavaScript-Konsole deines Browsers (meistens durch Drücken von `F12` oder `Strg+Shift+I`).
2. Kopiere den gesamten Skriptinhalt und füge ihn in die Konsole ein.
3. Drücke `Enter`, um das Skript auszuführen.

## Versionen
1. **Building_rename**
  - Verwendet nur Merkmale aus dem Punkt Merkmale
2. **Building_rename_Stadtzuordnung**
  - Hat zusätzlich eine Liste für die Stadtkürzel nach Opta hinterlegt. (Diese ist in Arbeit und noch recht klein. Wer hier zur Erweiterung beitragen möchte jederzeit gerne.)

## Konfiguration
Die folgenden Variablen können an die eigenen Bedürfnisse angepasst werden:
- **`NewBuildingCaption`**: Schema für die neuen Namen der Wachen. Platzhalter: 
  - `{DistrictAbbreviation}`: Landkreis-Kürzel
  - `{BOS}`: BOS-Einheit (z. B. Feuerwehr, Rettungsdienst)
  - `{Location}`: Name des Standorts
- **`FilterBuildingType`**: Array mit den Typen der zu ändernden Gebäude. Unterstützte Typen sind:
  - `0`: Feuerwache
  - `2`: Rettungswache
  - `6`: Polizeiwache
  - `9`: THW-Ortsverband
  - `18`: Feuerwache (Kleinwache)
  - `19`: Polizeiwache (Kleinwache)
  - `20`: Rettungswache (Kleinwache)

## Bekannte Fehler
- **Kreisfreie Städte**: Diese werden derzeit nicht korrekt erkannt. Eine Lösung für dieses Problem ist in Arbeit.

## Lizenz
Dieses Skript steht unter der **Attribution-NonCommercial-NoDerivs 4.0 Unported Lizenz**. Weitere Informationen zur Lizenz findest du [hier](http://creativecommons.org/licenses/by-nc-nd/4.0/).

---

**Autor**: MrGreenscreen aka. TiBo  
**Version**: 1.0  
**Copyright**: © 2024  
