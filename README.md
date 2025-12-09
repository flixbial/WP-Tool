# WP-Tool

# Heizungs-Vergleich mit CO₂-Kosten & Förderrechner

Dieses Projekt ist ein **Browser-Tool für Vermieter:innen**, mit dem sich ein Vergleich zwischen einer fossilen Heizung und einer Wärmepumpe über einen längeren Zeitraum (z. B. 20 Jahre) durchführen lässt.  

Berücksichtigt werden u. a.:

- Energieverbrauch und Gebäudefläche  
- CO₂-Preis-Szenarien (sehr niedrig bis sehr hoch)  
- Emissionsfaktoren verschiedener Energieträger  
- Vermieteranteil an CO₂-Kosten nach **CO₂KostAufG-Stufenmodell**  
- Investitionskosten, Wartung, Energiepreissteigerungen  
- Förderung von Wärmepumpen (vereinfacht nach BEG / KfW, inkl. KfW-Programm 522)  

Die Oberfläche ist komplett in HTML, CSS und JavaScript umgesetzt und läuft **ohne Backend** direkt im Browser.

---

## 🎯 Funktionen im Überblick

- Vergleich **fossile Heizung vs. Wärmepumpe** aus Vermietersicht  
- Automatische Berechnung der spezifischen CO₂-Emissionen in kg CO₂/m²a  
- Ermittlung des Vermieteranteils gemäß Stufenmodell (CO₂KostAufG)  
- Jährliche Kostenübersicht inkl. CO₂-Kostenanteil Vermieter  
- Kumulierte Kosten und einfache Amortisationszeit der Wärmepumpe  
- Vereinfachter **Förderrechner**:
  - Wohngebäude (KfW 458 – Grundförderung + Boni, gedeckelt nach Wohneinheiten)
  - Nichtwohngebäude (KfW 522 – Förderhöchstbetrag nach m² + Effizienzbonus)
- Grafische Auswertung:
  - Liniendiagramm: kumulierte Vermieterkosten fossil vs. Wärmepumpe (inkl. Breakeven-Punkt)
  - Balkendiagramm: Gesamtkosten im Betrachtungszeitraum
- Druckansicht zur Dokumentation (z. B. Gespräch mit Eigentümer:innen / Mieter:innen)

---

## 🧱 Technische Basis

- **index.html** – vollständige App (HTML + CSS + JS in einer Datei)
- Keine externen Abhängigkeiten, kein Build-Step nötig
- Läuft in jedem modernen Browser (Desktop, Tablet, Smartphone)
- Responsive durch `<meta name="viewport" content="width=device-width, initial-scale=1">`

---

## 🚀 Lokal ausführen

Du kannst das Tool lokal sehr einfach testen:

### Variante 1: Direkt öffnen
1. Repo klonen oder ZIP herunterladen  
2. `index.html` im Browser öffnen (Doppelklick)

> Hinweis: Einige Browser blockieren lokale Datei-Operationen/Module. In diesem Projekt wird kein Backend benötigt, daher funktioniert das in der Regel problemlos.

### Variante 2: Kleiner lokaler Webserver (empfohlen)

Mit Python (ab 3.x):

```bash
# Im Projektordner
python -m http.server 8000
