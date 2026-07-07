# Re-Use-Toolkit

Das Re-Use-Toolkit ist ein browserbasiertes Werkzeug für die überschlägige Bewertung der Wiederverwendung von Bauteilen. Es richtet sich an deutschsprachige Nutzerinnen und Nutzer und bleibt bewusst als einzelne statische HTML-Datei ohne Build-Schritt umgesetzt.

## Was das Werkzeug berechnet

Das Werkzeug enthält zwei Rechner:

1. **CO₂-Ersparnis durch Wiederverwendung von Bauteilen**
   Der Rechner schätzt, welche GWP-fossil-Emissionen aus der Neuproduktion vermieden werden, wenn ein gebrauchtes Bauteil wiederverwendet wird.

2. **Transport-Break-even**
   Der Rechner prüft, ab welcher einfachen Transportdistanz sich die Wiederverwendung eines gebrauchten Baustoffs oder Bauteils rechnerisch noch lohnt.

## Demo-Daten und Datenqualität

Alle aktuell enthaltenen Werte sind **Demo-Werte** in realistischer Größenordnung. Sie dürfen nicht als geprüfte oder verifizierte ÖKOBAUDAT-Werte verwendet werden.

Das Repository muss privat bleiben, bis die Demo-Werte durch verifizierte ÖKOBAUDAT-Daten ersetzt wurden. Der Demo-Hinweis im Werkzeug sollte erst nach Datenprüfung und Freigabe zur Veröffentlichung entfernt werden.

## Demo-Daten ersetzen

Alle Material- und Transportdaten liegen in `index.html` in zwei klar markierten JavaScript-Blöcken:

- `COMPONENTS`
- `TRANSPORT`

Zum Ersetzen der Demo-Daten:

1. Den Block `COMPONENTS` mit geprüften Bauteil- und Materialkennwerten aktualisieren.
2. Den Block `TRANSPORT` mit geprüften Transportkennwerten aktualisieren.
3. Die Annahmen und Hinweise im Werkzeug fachlich prüfen.
4. Erst nach Prüfung und Freigabe den Demo-Hinweis entfernen.

## Wichtige Felder in `COMPONENTS`

- `gwpNew`: GWP-fossil A1–A3 des neuen Produkts pro Einheit, angegeben in kg CO₂-Äquivalent pro Einheit.
- `mass`: Masse in kg pro Einheit. Dieser Wert wird für die Transportberechnung verwendet.
- `unit`: Einheit, die in der Oberfläche angezeigt wird, z. B. `Stück`, `m²`, `m³` oder `lfm`.
- `basis`: Kurze Annahme, die Nutzerinnen und Nutzern angezeigt wird, z. B. Abmessungen, Dicke oder Leistungsumfang.

## Annahme `REUSE_FACTOR`

Im Werkzeug gilt aktuell:

```js
REUSE_FACTOR = 0.95
```

Das bedeutet: Für Aufarbeitung, Reinigung und Vorbereitung wird pauschal ein Abschlag von 5 % auf die vermiedenen Emissionen angesetzt.

Diese Annahme ist eine vereinfachte Pauschale und muss vor einer Veröffentlichung mit verifizierten Daten fachlich geprüft werden.

## Deployment mit GitHub Pages

Die Anwendung liegt als `index.html` im Repository. Dadurch kann GitHub Pages die Datei direkt als statische Website ausliefern.

Es ist kein Build-Befehl erforderlich.

## Technische Rahmenbedingungen

- Single-file-Tool in deutscher Sprache.
- Keine externen Abhängigkeiten.
- Keine Package Manager.
- Keine Bundler oder Frameworks.
- Keine Analytics.
- Keine Cookies.
- Keine externen Schriftarten.

## Rechtlicher und organisatorischer Hinweis

Das Re-Use-Toolkit ist ein unabhängiges SURAP/BauMaB-Werkzeug und keine offizielle Anwendung des BMWSB oder BBSR.
