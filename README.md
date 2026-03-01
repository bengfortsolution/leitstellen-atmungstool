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

## So funktioniert das Tool (Kurz)

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

## Medizinisches Hintergrundwissen (verständlich erklärt)

### 1) Was ist ein „Atemzug“?
Ein Atemzug besteht aus **Einatmung + Ausatmung**. Gezählt wird jeweils **ein vollständiger Zyklus** (Brustkorb hebt sich und senkt sich wieder). :contentReference[oaicite:0]{index=0}

### 2) Wie misst man Atemfrequenz korrekt?
**Grundregel:**  
- Bei **regelmäßiger Atmung** kann man verkürzt zählen (z. B. **30 Sekunden** und hochrechnen).  
- Bei **unregelmäßiger Atmung** sollte man **die vollen 60 Sekunden** zählen, um den Mittelwert sauber zu erfassen. :contentReference[oaicite:1]{index=1}

**Praxis-Tipp:** Menschen verändern unbewusst ihre Atmung, wenn sie merken, dass man zählt. Deshalb wird in der Pflege oft empfohlen, nach dem Puls „unauffällig weiterzuzählen“. :contentReference[oaicite:2]{index=2}

### 3) Normwerte – Erwachsene
Für gesunde Erwachsene in Ruhe wird häufig ein Normalbereich von **12–20 Atemzügen pro Minute** angegeben. :contentReference[oaicite:3]{index=3}

### 4) Normwerte – Kinder (altersabhängig!)
Bei Kindern ist „normal“ stark vom Alter abhängig. Das Tool nutzt hierfür altersbezogene Referenzbereiche (PALS-Referenzkarte, 2025), z. B.: :contentReference[oaicite:4]{index=4}  
- Säugling (1–12 Monate): 30–53/min  
- Kleinkind (1–2 Jahre): 22–37/min  
- Vorschulkind (3–5 Jahre): 20–29/min  
- Schulkind (6–12 Jahre): 18–25/min  
- Jugendliche (13–17 Jahre): 12–20/min

### 5) Warum eine „Frühwarnung“ bei „kein Atemzug seit X Sekunden“?
In der Schlafmedizin/Physiologie wird „Apnoe“ häufig als **Atem-/Luftstrom-Ausfall über ≥10 Sekunden** definiert (z. B. AASM-orientierte Definitionen). :contentReference[oaicite:5]{index=5}

**Wichtig:** Im Leitstellenkontext ist das im Tool als **Frühwarnsignal** gedacht, nicht als endgültige Diagnose.  
Ziel ist: **Zeit sparen**, wenn die Situation hochkritisch erscheint (z. B. bewusstlos + keine normale Atmung) – die konkrete Handlung richtet sich immer nach euren SOPs.

---

## Was das Tool NICHT ist (wichtiger Hinweis)
- Kein Medizinprodukt und kein Ersatz für klinische Beurteilung
- Keine automatische Diagnose
- Keine Abweichung von Leitstellen-SOPs / Protokollen
- Das Tool unterstützt nur die **Erfassung & Sichtbarmachung** der Atemfrequenz und von Warnmustern.

---

## Technik (kurz)
- Statische Web-App (`index.html`, `style.css`)
- Keine externen Abhängigkeiten (läuft auch offline/intern)
- Optimiert für Desktop: **Leertaste**, **U**, **R**
- Berechnung:
  - frühe Schätzung anhand der letzten Atemzug-Abstände
  - Stabilisierung mit zunehmender Messdauer (bis 60 Sekunden)

---

## Quellen / Referenzen

- Normaler Erwachsenennormalbereich: 12–20/min (Übersichtsartikel). :contentReference[oaicite:6]{index=6}  
- Zählmethode: 30 Sekunden bei regelmäßiger Atmung, 60 Sekunden bei unregelmäßiger Atmung; Definition eines Atemzugs (Ein- + Ausatmung). :contentReference[oaicite:7]{index=7}  
- Pädiatrische Normwerte nach Altersgruppen (PALS 2025 Referenzkarte). :contentReference[oaicite:8]{index=8}  
- Apnoe-Definition (≥10 Sekunden Luftstrom-Abfall/Stillstand, schlafmedizinische Standarddefinitionen). :contentReference[oaicite:9]{index=9}  

---

## Lizenz / Nutzung
(Tragt hier eure gewünschte Lizenz ein – z. B. MIT, Apache-2.0 oder „intern“.)

---

## Kontakt
Bengfort Solution – Projekt/Team: (hier eintragen)
