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
