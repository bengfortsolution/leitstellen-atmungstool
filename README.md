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


📊 Schwellenwerte Atemfrequenz (RR)
👤 Erwachsene
Bereich	Atemfrequenz (/min)	Bedeutung
🔴 Kritisch niedrig	< 6	Hochgradig auffällig, vitale Gefährdung möglich
🟡 Niedrig	6–9	Bradypnoe, Kontext prüfen
🟢 Normal	12–20	Erwartbarer Ruhebereich
🟡 Erhöht	21–30	Tachypnoe, mögliche Belastung / Dyspnoe
🔴 Sehr hoch	> 30	Deutlich auffällig, schwere Atemnot möglich

Frühwarnung:
🔴 Kein Atemzug seit ≥ 10 Sekunden

👶 Kinder (altersabhängig)
Säugling (1–12 Monate)
Bereich	Atemfrequenz (/min)
🔴 Deutlich zu niedrig	< 24
🟢 Normal	30–53
🔴 Deutlich zu hoch	> 63

Frühwarnung: ≥ 10 Sekunden kein Atemzug

Kleinkind (1–2 Jahre)
Bereich	Atemfrequenz (/min)
🔴 Deutlich zu niedrig	< 16
🟢 Normal	22–37
🔴 Deutlich zu hoch	> 47

Frühwarnung: ≥ 10 Sekunden kein Atemzug

Vorschulkind (3–5 Jahre)
Bereich	Atemfrequenz (/min)
🔴 Deutlich zu niedrig	< 14
🟢 Normal	20–29
🔴 Deutlich zu hoch	> 39

Frühwarnung: ≥ 10 Sekunden kein Atemzug

Schulkind (6–12 Jahre)
Bereich	Atemfrequenz (/min)
🔴 Deutlich zu niedrig	< 12
🟢 Normal	18–25
🔴 Deutlich zu hoch	> 35

Frühwarnung: ≥ 10 Sekunden kein Atemzug

Jugendliche (13–17 Jahre)
Bereich	Atemfrequenz (/min)
🔴 Deutlich zu niedrig	< 8
🟢 Normal	12–20
🔴 Deutlich zu hoch	> 30

Frühwarnung: ≥ 10 Sekunden kein Atemzug

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
