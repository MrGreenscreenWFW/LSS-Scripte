
# Fahrzeug-Umbenennungsskript

Dieses Skript dient zur automatischen Umbenennung von Fahrzeugen im Spiel "Leitstellenspiel" gemäß den angegebenen Einstellungen.

## Funktionen

- Automatische Umbenennung aller Fahrzeuge basierend auf einem einstellbaren Namensschema.
- Unterstützung für eine Vielzahl von Fahrzeugtypen.
- Option, Nummerierungen nur dann hinzuzufügen, wenn mehr als ein Fahrzeug desselben Typs vorhanden ist.

## Anforderungen

- Ein Benutzerkonto bei [Leitstellenspiel](https://www.leitstellenspiel.de).
- Ein aktueller Webbrowser mit Unterstützung für JavaScript.
- Ein gültiger CSRF-Token, der automatisch aus der Webseite abgerufen wird.

## Einstellungen

Die Einstellungen des Skripts befinden sich am Anfang der Datei und können angepasst werden:

```javascript
// Platzhalter: {Building}, {VehicleName}, {VehicleType}, {Index}
var NewCaption = '{Building} / {VehicleType}/{Index}';

// Hinzufügen von Zahlen nur, wenn mehr als ein Fahrzeug desselben Typs vorhanden ist
var AddNumbersOnlyIfMultiple = true;
```

### Platzhalter:

- `{Building}`: Name des Gebäudes, zu dem das Fahrzeug gehört.
- `{VehicleType}`: Typ des Fahrzeugs (z. B. "LF", "RTW").
- `{Index}`: Nummer des Fahrzeugs (optional, abhängig von `AddNumbersOnlyIfMultiple`).

### `AddNumbersOnlyIfMultiple`

Wenn `true`, werden Nummerierungen nur dann hinzugefügt, wenn es mehr als ein Fahrzeug desselben Typs gibt.

## Fahrzeugtypen

Das Skript unterstützt eine große Liste von Fahrzeugtypen. Eine vollständige Übersicht findest du direkt im Code im Abschnitt `vehicleTypeMapping`.

## Nutzung

1. Kopiere den Skriptcode in die Browser-Konsole auf der Seite von Leitstellenspiel.
2. Führe das Skript aus.
3. Die Fahrzeugnamen werden entsprechend der Einstellungen automatisch geändert.

## Haftungsausschluss

Dieses Skript ist ausschließlich für den persönlichen Gebrauch gedacht. Es wird keine Garantie für die Funktionalität oder mögliche Konsequenzen durch die Nutzung übernommen. Verwende das Skript auf eigene Verantwortung.

## Lizenz

Dieses Skript steht unter der **Attribution-NonCommercial-NoDerivs 4.0 International (CC BY-NC-ND 4.0)** Lizenz. Weitere Informationen findest du [hier](http://creativecommons.org/licenses/by-nc-nd/4.0/).
