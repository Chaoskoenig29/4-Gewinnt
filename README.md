# Vier Gewinnt

Ein responsives, deutschsprachiges 4-Gewinnt-Spiel ohne Build-Schritt und ohne externe Laufzeit-Abhängigkeiten.

## Starten

1. Repository klonen oder herunterladen.
2. `index.html` in einem aktuellen Browser öffnen. Für zuverlässige BroadcastChannel-Räume bitte über einen lokalen Webserver starten, z. B. `python3 -m http.server 8000`, dann `http://localhost:8000` aufrufen.
3. Modus **Lokal**, **KI-Gegner** oder **Online** wählen. Online: Raum erstellen und den sechsstelligen Code in einem zweiten Tab desselben Browsers eingeben. Die Raumkommunikation verwendet BroadcastChannel und funktioniert deshalb nur zwischen Tabs desselben Browsers/Origins, nicht über das Internet zwischen Geräten. Für echte Online-Räume ist ein Signalisierungs-/Relay-Backend erforderlich.

## Funktionen

- 7×6-Spielbrett, Fallanimation, Sieg-/Remis-Erkennung und hervorgehobene Gewinnreihe
- Lokales Zwei-Spieler-Spiel und KI mit leichtem, mittlerem und schwerem Minimax-Modus
- Private Tab-Räume per Einladungscode (BroadcastChannel, gleicher Browser/Origin)
- Deutsche Spot-Sprüche per Browser-Sprachausgabe; Sprachausgabe ist über den Lautsprecher-Schalter deaktivierbar
- Siege, gespielte Partien, Remis und letzte Ergebnisse werden lokal im Browser gespeichert
- Responsive Layout, Tastatur-/Screenreader-Beschriftungen und reduzierte Bewegung bei entsprechender Systemeinstellung

## Tests

Mit Node.js (ohne zusätzliche Pakete):

```sh
node --test
```

Die Tests prüfen grundlegende Spielregeln, ungültige Züge, Siege in mehreren Richtungen, Remis und KI-Züge.
