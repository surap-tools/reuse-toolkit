# Re-Use-Toolkit

Das Re-Use-Toolkit ist ein leichtgewichtiges, browserbasiertes Werkzeug zur überschlägigen Bewertung der Wiederverwendung von Bauteilen. Es ist Teil der „SURAP Open Source Tools“ und bleibt bewusst als einzelne statische HTML-Datei ohne Build-Schritt umgesetzt.

## Tool öffnen

[Tool testen](https://surap-tools.github.io/reuse-toolkit/)

## Was macht das Tool?

Das Tool zeigt, welche Treibhausgasemissionen durch die Wiederverwendung ausgewählter Bauteile rechnerisch vermieden werden können. Zusätzlich kann abgeschätzt werden, bis zu welcher Transportdistanz die Wiederverwendung trotz Transportemissionen klimapositiv bleibt.

## Funktionen

- Rechner für die CO₂-Ersparnis durch Wiederverwendung gegenüber einem Neukauf.
- Transport-Break-even-Rechner für einfache Strecken oder Hin- und Rückfahrten.
- Auswahl mehrerer Bauteilgruppen mit Mengenangabe je passender Einheit.
- Anzeige der zugrunde gelegten Bauteilannahmen, Gesamtmasse und einfachen Ergebnisinterpretation.
- Demo-Hinweis direkt im Tool sowie klar markierte Datenblöcke `COMPONENTS` und `TRANSPORT` im Quelltext.

## Datenstatus

Die aktuellen Daten sind Demo-Daten in realistischer Größenordnung. Die Datenblöcke `COMPONENTS` und `TRANSPORT` sind im Quelltext entsprechend markiert.

Die aktuellen Werte dienen nur zu Demonstrations- und Testzwecken und dürfen nicht als geprüfte ÖKOBAUDAT-Werte interpretiert werden.

Hinweis: Das Tool ist technisch bereits testbar. Vor einer öffentlichen fachlichen Nutzung müssen die Demo-Werte durch geprüfte Daten ersetzt und die Demo-Hinweise entfernt oder angepasst werden.

## Datenquellen

Datenquellen müssen geprüft, versioniert und nachvollziehbar dokumentiert werden.

Wenn echte ÖKOBAUDAT-Daten eingesetzt werden, ist die Version zu ergänzen:

Datenquelle: ÖKOBAUDAT [Version eintragen], BMWSB/BBSR.

## Methodische Annahmen

- Das Tool betrachtet eine überschlägige Vermeidung von GWP-fossil-Emissionen aus der Neuproduktion in A1–A3.
- Für Wiederverwendung wird aktuell ein pauschaler Faktor `REUSE_FACTOR = 0.95` genutzt. Damit wird ein Abschlag von 5 % für Aufarbeitung, Reinigung und Vorbereitung angesetzt.
- Die Transportberechnung nutzt Demo-Emissionsfaktoren je Fahrzeugkilometer und Demo-Nutzlasten aus dem Block `TRANSPORT`.
- Bei der Transportberechnung wird die erforderliche Fahrtenzahl aus Gesamtmasse und Nutzlast abgeschätzt.
- Die Option „Leere Rückfahrt mitrechnen“ verdoppelt die eingegebene einfache Strecke für die Transportemissionen.
- Die angezeigten PKW-Kilometer dienen nur der Anschaulichkeit.

## Grenzen des Tools

- Das Tool ersetzt keine vollständige Gebäudeökobilanz.
- Das Tool ersetzt keine prüffähige Zertifizierung oder projektspezifische Fachprüfung.
- Die aktuellen Demo-Werte sind nicht für fachliche Nachweise geeignet.
- Projektspezifische Themen wie Rückbau, Qualitätsprüfung, Schadstoffe, Lagerung, Montage, Verluste oder detaillierte Lebenszyklusmodule werden nicht vollständig abgebildet.

## Deployment

Das Tool wird als statische GitHub-Pages-Anwendung bereitgestellt.

Das Tool benötigt keinen Build-Schritt. Es kann über GitHub Pages direkt aus `index.html` bereitgestellt werden.

## Lizenz

Code: Apache-2.0.

Daten: siehe jeweilige Quellen- und Datenhinweise.

## Kontakt

SURAP GmbH  
https://www.surap.de
