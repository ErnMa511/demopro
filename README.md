# 🏍️ Motorrad-Wetteranzeige mit Node-RED

## 🎯 Projektziel

Dieses Projekt zeigt Motorradfahrern auf einen Blick, ob das Wetter aktuell **für eine Fahrt geeignet ist oder nicht**. 

Basierend auf **Live-Wetterdaten** wie Regen, Wind und Temperatur trifft das System automatisch eine Entscheidung und zeigt diese visuell auf einem Bildschirm an (z. B. als Dashboard auf einem Raspberry Pi oder PC).  

Das Ziel: **"Kann ich heute Motorrad fahren?" – in einer Sekunde beantwortet.**

---

## 🛠️ Verwendete Technologien

- **Node-RED** – visuelle Programmierumgebung
- **OpenWeatherMap API** – zur Abfrage von aktuellen Wetterdaten
- **Node-RED Dashboard** – zur Darstellung der Auswertung
- **JavaScript** – für Entscheidungslogik in Function-Nodes
- (Optional) **Raspberry Pi mit Display** – für eine lokale Anzeige

---

## 🧠 Projektphasen & Arbeitsschritte

### 📌 Phase 1: Zieldefinition & Anforderungen
- Relevante Wetterfaktoren bestimmen: Regen, Wind, Temperatur
- Entscheidungskriterien definieren (ab wann ist es gefährlich?)
- Anzeigeform überlegen (Text, Farbe, Icon, Ampel-Logik)

---

### ☁️ Phase 2: Wetterdaten integrieren
- OpenWeatherMap-API-Key generieren
- Node-RED HTTP-Request-Node verwenden
- Daten aus JSON extrahieren (z. B. `wind.speed`, `rain.1h`)

---

### 🧮 Phase 3: Entscheidungslogik
- Beispiel-Regeln:
  - `Regen > 0 mm` → ❌ *Nicht fahren*
  - `Wind > 40 km/h` → ⚠️ *Achtung*
  - `Temp < 5°C` → ⚠️ *Sehr kalt*
- Logik mit Function-Node (JavaScript) umsetzen

---

### 📊 Phase 4: Anzeige & Benutzeroberfläche
- Node-RED Dashboard-Nodes nutzen
- Klare Visualisierung:
  - ✅ **Fahren möglich**
  - ❌ **Nicht fahren empfohlen**
  - ⚠️ **Mit Vorsicht fahren**
- Farben & Symbole für schnelle Erfassung

---

### 🔁 Phase 5: Test & Optimierung
- Verschiedene Wettersituationen durchtesten
- Anzeige auf mobilen Geräten prüfen
- Schwellenwerte feinjustieren

---

### 📝 Phase 6: Dokumentation & Veröffentlichung
- Diese README schreiben ✍️
- Screenshots vom Dashboard hinzufügen
- GitHub-Projekt veröffentlichen

---

## 💡 Warum ist dieses Projekt besonders?

🚀 **Alltagsnutzen:** Motorradfahrer erhalten eine direkte Entscheidungshilfe – ohne selbst Wetterdaten interpretieren zu müssen.  
🧩 **Modular & erweiterbar:** Leicht anpassbar für Roller, E-Bikes oder sogar Autofahrer.  
🎨 **Benutzerfreundlich:** Klare Anzeige statt langer Wetterberichte.  
📦 **Open Source:** Einfach zum Nachbauen oder Erweitern.

---

## 🧪 Erweiterungsideen

- Telegram/Push-Benachrichtigung bei Wetteränderung
- Sprachsteuerung („Kann ich fahren?“ → „Nein, zu starker Wind“)
- Historische Wetterdaten analysieren
- Integration in Smart-Home-Systeme (z. B. über MQTT)

---

> **Tipp:** Der Code für die Entscheidungslogik befindet sich im Flow-Ordner. API-Zugangsdaten müssen über Umgebungsvariablen gesetzt werden.
