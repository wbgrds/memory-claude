# Memory-Cleanup-Plan — 2026-09-19

## 🔍 Status Quo

**Aktuelle Situation:**
- 40+ Memory-Dateien
- Kontext-Overflow in Claude App (mobile)
- Token-Fenster zu klein für neue Requests + alle Memory

**Ursache:**
- `/areas/` — 16 Projektdateien (teilweise inaktiv)
- `/people/` — 10+ Kontakt-Dateien (zu granular)
- `/topics/` — 15+ Topic-Dateien (redundant, alt)
- `/projects/` — 11 Project-Ordner (gemischt aktiv/archiviert)

---

## ✅ KEEPLIST — Bleibt bestehen (aktiv täglich)

### Profile & Basis
- `profile.md` — Basis: Olaf Scharfenberg, Geschäftsführer, 4-Tage-Woche
- `claude-md-main.md` — CLAUDE.md Reference (falls noch nicht in KaI)

### Aktive Areas (täglich im Einsatz)
- `korbgraal-app.md` — Ulrich Rosenke, Android-App, Tests täglich (Samsung Galaxy Tab S6)
- `kai-repo.md` — **Die** Single Source of Truth, alle Projekte
- `merchandise.md` — WEBGUARDS Merch-Linie

### OB5 Strategie (3 Dateien, aber zusammenfassbar)
- `ob5-holding-strategy.md` — Übergeordnet
- (Die anderen 2 `ob5-*.md` → in diese mergen oder archivieren)

### Wichtigste Topics
- `engelkinder-status.md` — Mia & Julia, §8a SGB VIII (Sept 2026)
- `vater-ohne-kinder.md` — Kern-Identität für "Zwischen Pflicht und Gefühl"

### Integrations (aktiv genutzt)
- `sipgate-oauth2-credentials.md` — React Dashboard
- `twilio-credentials.md` — WhatsApp Integration

### Persönliches (längerfristig)
- `autobiographie.md` — "Zwischen Pflicht und Gefühl" (E00–E25)
- `unternehmergesellschaft-book.md` — KDP Buchreihe

### Key People (nur essentiell)
- `nadine.md` — Partnerin
- `hans-rosenthal.md` — Ennys Lounge / Teammitglied
- `ulrich-rosenke.md` — Korbgraal Kunde

---

## ❌ DELETELIST — Raus (redundant, alt, abgeschlossen)

### Topics (zu viel Metadaten)
- `schreibweise-fallen.md` — alte Dokumentation (ersetzen durch Habits im Prompt)
- `recent-work.md` — kurzlebig, veraltet
- `inbox-struktur.md` — alt, nicht mehr relevant
- `claude-md-main.md` — (wenn Duplkat zu KaI/CLAUDE.md)
- `claude-regeln.md` — Doppelt zu `claude-md-main.md`
- `calendar-event-intake-skill.md` — experimentell, nicht umgesetzt
- `cell-father-song.md` — Kontext-Info, kein Handlungsbedarf

### Areas (überprüfung notwendig)
- `ennys-grow-store.md` — läuft noch?
- `help-webguards.md` — aktiv gepflegt?
- `gps-location-tracker.md` — in Produktion?
- `sipgate-gtm-strategy.md` — archiviert oder aktuell?
- `sipgate-dashboard-readme.md` — veraltet durch neue Versionen?

### People (zu granular, ersetzen durch 1–2 Notizen)
- `christoph-mader.md` — Sipgate Partner Manager (nur falls aktive Deals)
- `dana-hinz.md` — Sozialarbeiterin Impuls e.V. (historisch?)
- `elisabeth.md` — Familienglied (ersetzen durch `/areas/enkelkinder-dossier.md`)
- `kristina-schulz.md` — Anwältin (nicht aktiv derzeit)
- `rene-bartz.md`, `rene-bartz-pieroth.md` — Doppel-Eintrag (1 reicht)
- `ronald-wende.md` — Kunde (historisch, abgeschlossen?)
- `vanessa-turlach.md` — Marketing WEBGUARDS (noch aktiv?)

### Projects Ordner (CHECKLIST: Olaf beantworten)
```
/projects/019de414.../ — Tochterfirma Hans → Ist das noch laufend?
/projects/019df9f9.../ — SELBSTSPIEGEL (Custody) → Abgeschlossen 2026?
/projects/019dfd77.../ — Konfiguration Claude → Ist das noch in Arbeit?
/projects/019dfe38.../ — Rosenke Projekte → Läuft noch?
/projects/019dfe3e.../ — Kundenprojekte → Welche sind aktiv?
/projects/019dfe45.../ — Webentwicklung → Status?
/projects/019dff00.../ — Skills (Zenkit/easybell) → Noch relevant?
/projects/019e39f1.../ — Privates Buch → Subsumiert von autobiographie.md?
/projects/019e6d80.../ — Snippets → Was ist das noch?
/projects/019e92e0.../ — Buch: UG → Läuft parallel zu unternehmergesellschaft-book.md?
/projects/019e9860.../ — Generalorgie → Genealogische Forschung aktiv?
/projects/019ef467.../ — Kommunikation → GitHub/KaI abgegolten?
/projects/019ef7f6.../ — GitHub Repos → Subsumiert von KaI?
/projects/019f411d.../ — Büro Organisation → Redundant zu KaI?
/projects/019f4bb2.../ — Ideen Auswertung → Noch relevant?
/projects/019f5ab9.../ — WEBSITES → Welche? (ob5.de, help.webguards.de?)
/projects/019f8ac0.../ — Rosenke (duplicate?) → Doppelt zu 019dfe38?
/projects/019f8c79.../ — Familie → EnkelkinderDossier?
/projects/019faffd.../ — Wohngeld → Status 2026?
/projects/019fd7d1.../ — MCP Hub → In Produktion?
/projects/01a0875f.../ — (leer?)
/projects/01a0b8f9.../ — Elterntreffen KW41 → Vorbei?
```

---

## 🎯 Aufräum-Strategie

### Phase 1: Definitionen klären (Olaf antwortet)
1. Welche `/areas/` sind **wirklich täglich** aktiv?
2. Welche `/people/` brauchst du im Memory vs. GitHub/CRM?
3. Welche `/projects/` sind archiviert/done vs. laufend?
4. Soll `/projects/` ganz raus oder zu Sammel-Dateien konsolidiert?

### Phase 2: Cleanup ausführen
1. Identifizierte Files löschen
2. Redundante Einträge mergen
3. Memory in Claude App refreshen
4. Performance testen

### Phase 3: Struktur neu definieren
- 10–12 aktive Memory-Dateien max
- Klare Kategorien: Profile, Areas (aktiv), People (essentiell), Topics (täglich)
- `kai-repo.md` als Verweis für alles andere (Projects leben in GitHub)

---

## ❓ Klärungsfragen für Olaf

**Vor dem Löschen antworten:**

1. **Ennys Grow Store** — läuft noch?
2. **WEBGUARDS Help Center** — wird gepflegt?
3. **GPS Location Tracker** — in Produktion oder Experiment?
4. **Sipgate Dashboard** — ist die README aktuell?
5. **Ronald Wende** — noch aktiver Kunde (Profil-Site)?
6. **SELBSTSPIEGEL Projekt** — abgeschlossen oder laufend?
7. **Alle `/projects/` in der Liste oben** — Haken setzen: ✅ (läuft noch) oder ❌ (archiviert)
8. **Genealogische Forschung (Generalorgie)** — aktiv oder pausiert?

---

## 📊 Zielzustand nach Cleanup

```
/profile.md                                     (1 Datei)
/areas/kai-repo.md                              (1 Datei)
/areas/korbgraal-app.md                         (1 Datei)
/areas/merchandise.md                           (1 Datei)
/areas/ob5-holding-strategy.md                  (1 Datei, konsolidiert)
/areas/autobiographie.md                        (1 Datei)
/areas/unternehmergesellschaft-book.md          (1 Datei)
/areas/enkelkinder-dossier.md                   (1 Datei)
/topics/engelkinder-status.md                   (1 Datei)
/topics/vater-ohne-kinder.md                    (1 Datei)
/integrations/sipgate-oauth2-credentials.md    (1 Datei)
/integrations/twilio-credentials.md            (1 Datei)
/people/nadine.md                               (1 Datei)
/people/hans-rosenthal.md                       (1 Datei)
/people/ulrich-rosenke.md                       (1 Datei)

TOTAL: ~15 Dateien (statt 40+)
Kontext-Savings: ~60–70%
```

---

## 🚀 Nächste Schritte

1. ✅ Diesen Plan im `wbgrds/memory-claude` Repo speichern
2. ⏳ **Olaf**: Klärungsfragen beantworten (CLEANUP-CHECKLIST.md)
3. 🔄 Claude: Basierend auf Antworten → MEMORY-STRUCTURE.md schreiben
4. 🗑️ Claude: Memory-Dateien in Claude App löschen / neu strukturieren
5. ✨ Test: Neuer Chat, kein Kontext-Overflow mehr
