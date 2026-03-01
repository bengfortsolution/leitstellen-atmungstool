# Atmungstool (Leitstelle) – Atemfrequenz schnell & sicher erfassen

Dieses Tool unterstützt Disponentinnen und Disponenten dabei, die **Atemfrequenz (AF/RR)** bei **Erwachsenen und Kindern** schnell zu erfassen und Auffälligkeiten früh zu erkennen – insbesondere Situationen, in denen **seit mehreren Sekunden kein Atemzug** beobachtet wird (Frühwarnung).

Das Tool ist als **statische Web-Anwendung** ausgelegt (nur `index.html` + `style.css`) und kann sehr einfach über **NGINX** bereitgestellt werden.

---

## Warum ist Atemfrequenz so wichtig?

Die Atemfrequenz gehört zu den wichtigsten Vitalparametern. Auffällige Werte können ein Hinweis sein auf:
- Atemwegsprobleme / Atemnot
- Schock / Sepsis
- neurologische Ereignisse
- Intoxikation, metabolische Entgleisung
- Überforderung, Panik/Hyperventilation

**Wichtig:** Die Atemfrequenz wird in der Praxis häufig ungenau erhoben. Genau hier hilft das Tool: **schnelle, reproduzierbare Erfassung** und klare Darstellung.

---

## Zielgruppe & Einsatz

**Zielgruppe:** Leitstelle / Disposition (Desktop, Browser, Maus + Tastatur)

**Einsatz:** Unterstützt beim Telefonat/Abfragen, wenn eine Person beobachtet wird (z. B. durch Anrufer vor Ort), oder wenn im Leitstellen-Setting Atemzüge gezählt werden sollen.

---

## So funktioniert das Tool (Kurzfassung)

1. **Patientengruppe wählen**
   - **Erwachsene**
   - **Kind** (mit Altersgruppe)

2. **Jeden Atemzug erfassen**
   - Klick auf „Atemzug erfassen“ oder **Leertaste**
   - (Optional) **Rückgängig** mit „U“
   - **Reset** mit „R“

3. Das Tool zeigt:
   - **Atemfrequenz (/min)** als laufende Berechnung
   - **Zeit seit letztem Atemzug**
   - **Verlauf der Atemzug-Abstände**
   - **Ampelbewertung** (Norm / auffällig)

4. **Frühwarnung (starker Alarm)**
   - Wenn **seit X Sekunden kein Atemzug** erfasst wurde, wird ein **roter Alarm** ausgelöst:
     - sehr auffälliges Warnbanner (blinkend)
     - akustisches Signal (Browser)
     - Tab-Titel wird markiert (🚨)

> Der Alarm stoppt automatisch, sobald wieder ein Atemzug erfasst wird.  
> (Optional kann man das später auf „Quittieren erforderlich“ umbauen, wenn gewünscht.)



# 📊 Schwellenwerte Atemfrequenz (RR)

Diese Tabelle dient als Referenz für das Atmungstool.  
Die Bewertung ersetzt **keine medizinische Gesamtbeurteilung** und erfolgt stets im Kontext.

---

## 👤 Erwachsene

| Bereich | Atemfrequenz (/min) | Bewertung |
|----------|--------------------|------------|
| 🔴 Kritisch niedrig | < 6 | Hochgradig auffällig, vitale Gefährdung möglich |
| 🟡 Niedrig | 6–9 | Bradypnoe, Kontext prüfen |
| 🟢 Normal | 12–20 | Erwartbarer Ruhebereich |
| 🟡 Erhöht | 21–30 | Tachypnoe, mögliche Belastung / Dyspnoe |
| 🔴 Sehr hoch | > 30 | Deutlich auffällig, schwere Atemnot möglich |

**Frühwarnung:**  
🔴 Kein Atemzug seit ≥ 10 Sekunden

---

## 👶 Kinder (altersabhängig)

### Säugling (1–12 Monate)

| Bereich | Atemfrequenz (/min) | Bewertung |
|----------|--------------------|------------|
| 🔴 Deutlich zu niedrig | < 24 | Bradypnoe, hoch auffällig |
| 🟢 Normal | 30–53 | Altersentsprechend |
| 🔴 Deutlich zu hoch | > 63 | Deutlich erhöhte Atemfrequenz |

**Frühwarnung:** Kein Atemzug seit ≥ 10 Sekunden

---

### Kleinkind (1–2 Jahre)

| Bereich | Atemfrequenz (/min) | Bewertung |
|----------|--------------------|------------|
| 🔴 Deutlich zu niedrig | < 16 | Bradypnoe |
| 🟢 Normal | 22–37 | Altersentsprechend |
| 🔴 Deutlich zu hoch | > 47 | Deutlich erhöhte Atemfrequenz |

**Frühwarnung:** Kein Atemzug seit ≥ 10 Sekunden

---

### Vorschulkind (3–5 Jahre)

| Bereich | Atemfrequenz (/min) | Bewertung |
|----------|--------------------|------------|
| 🔴 Deutlich zu niedrig | < 14 | Bradypnoe |
| 🟢 Normal | 20–29 | Altersentsprechend |
| 🔴 Deutlich zu hoch | > 39 | Deutlich erhöhte Atemfrequenz |

**Frühwarnung:** Kein Atemzug seit ≥ 10 Sekunden

---

### Schulkind (6–12 Jahre)

| Bereich | Atemfrequenz (/min) | Bewertung |
|----------|--------------------|------------|
| 🔴 Deutlich zu niedrig | < 12 | Bradypnoe |
| 🟢 Normal | 18–25 | Altersentsprechend |
| 🔴 Deutlich zu hoch | > 35 | Deutlich erhöhte Atemfrequenz |

**Frühwarnung:** Kein Atemzug seit ≥ 10 Sekunden

---

### Jugendliche (13–17 Jahre)

| Bereich | Atemfrequenz (/min) | Bewertung |
|----------|--------------------|------------|
| 🔴 Deutlich zu niedrig | < 8 | Bradypnoe |
| 🟢 Normal | 12–20 | Altersentsprechend |
| 🔴 Deutlich zu hoch | > 30 | Deutlich erhöhte Atemfrequenz |

**Frühwarnung:** Kein Atemzug seit ≥ 10 Sekunden

---

## 🧠 Hinweise zur Messung

- Bei regelmäßiger Atmung: 30 Sekunden zählen und hochrechnen möglich  
- Bei unregelmäßiger Atmung: möglichst 60 Sekunden vollständig zählen  
- Bewertung immer im Kontext (Fieber, Belastung, Schlaf, Medikamente, Intoxikation etc.)  
- Die 10-Sekunden-Schwelle ist eine Frühwarnung, keine alleinige Diagnose
---



## Was das Tool NICHT ist (wichtiger Hinweis)
- Kein Medizinprodukt und kein Ersatz für klinische Beurteilung
- Keine automatische Diagnose
- Keine Abweichung von Leitstellen-SOPs / Protokollen
- Das Tool unterstützt nur die **Erfassung & Sichtbarmachung** der Atemfrequenz und von Warnmustern.

---

## Technik (kurzfassung)
- Statische Web-App (`index.html`, `style.css`)
- Keine externen Abhängigkeiten (läuft auch offline/intern)
- Optimiert für Desktop: **Leertaste**, **U**, **R**
- Berechnung:
  - frühe Schätzung anhand der letzten Atemzug-Abstände
  - Stabilisierung mit zunehmender Messdauer (bis 60 Sekunden)

---

## Quellen / Referenzen


- Pädiatrische Normwerte nach Altersgruppen (PALS 2025 Referenzkarte). https://guidelines.redcross.org/wp-content/uploads/2025/12/PALS-Pediatric-Systematic-Assessment.pdf


---



---

## Kontakt
Bengfort Solution
