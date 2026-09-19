# Claude Memory Backup — Hybrid Approach

**Status:** INCOMPLETE — Struktur vorbereitet, Inhalte benötigen manuellen Export

---

## Was ist hier?

```
memory-backup/
├── profile.md                 # COMPLETE (auto-reconstructed)
├── areas/                     # Projects, domains, active work
├── people/                    # Contacts (colleagues, family, customers)
├── topics/                    # Knowledge, patterns, interests
├── projects/                  # Named projects (21 files)
└── integrations/              # Credentials & API configs (SENSITIVE)
```

## Datei-Status

- **COMPLETE**: `profile.md` — vollständig rekonstruiert aus System-Kontext
- **PLACEHOLDER**: Alle anderen — nur Metadaten (Pfad, Beschreibung, lastUpdated)
- **SENSITIVE**: `integrations/` — Credentials nicht exportiert, manuell nur in Private Repo

---

## Wie wird das fertig?

### Option A: Automatischer Export (nicht möglich)
Claude kann seine Memory-Dateien nicht direkt zugreifen — nur Struktur/Metadaten sichtbar.

### Option B: Manueller Export (empfohlen)
1. **In Claude App öffnen:** https://claude.ai/settings/memory
2. **Export-Funktion nutzen** (falls verfügbar in Desktop/Web App)
3. **Dateien herunterladen** → `/memory-backup/` kopieren
4. **Ordner-Struktur beibehalten:**
   ```
   memory-backup/
   ├── profile.md
   ├── areas/
   │   ├── autobiographie.md
   │   ├── kai-repo.md
   │   └── ... (16 files)
   ├── people/
   │   ├── hans-rosenthal.md
   │   ├── nadine.md
   │   └── ... (10 files)
   ├── topics/
   │   ├── engelkinder-status.md
   │   ├── vater-ohne-kinder.md
   │   └── ... (13 files)
   ├── projects/
   │   └── ... (21 files)
   └── integrations/
       ├── sipgate-oauth2-credentials.md  [SENSITIVE]
       └── twilio-credentials.md           [SENSITIVE]
   ```

### Option C: Hybrid (aktuell implementiert)
1. ✅ `MEMORY-MANIFEST.json` — komplette Struktur + Metadaten
2. ✅ `profile.md` — rekonstruiert aus System-Kontext
3. 🔄 **In Arbeit:** Manueller Export der restlichen 39 Dateien
4. 📋 **Dann:** `CLEANUP-CHECKLIST.md` ausfüllen, Delete-Kandidaten prüfen

---

## Nächste Schritte

1. **Schritt 1:** Diesen Ordner mit den echten Memory-Dateien bestücken
   ```bash
   # Wenn auto-Export verfügbar:
   cp ~/claude-memory-export/* ./memory-backup/
   
   # Sonst: manuell aus Claude App exportieren
   ```

2. **Schritt 2:** `CLEANUP-CHECKLIST.md` ausfüllen
   ```bash
   # In diesem Repo:
   git checkout CLEANUP-CHECKLIST.md
   # ... Fragen beantworten ...
   git add CLEANUP-CHECKLIST.md
   git commit -m "Cleanup-Entscheidungen: Areas, People, Topics, Projects"
   ```

3. **Schritt 3:** `MEMORY-STRUCTURE.md` erzeugen
   - Soll-Zustand (Keep-List: ~15 Dateien)
   - Delete-Liste (Candidate: 8–12 Dateien)

4. **Schritt 4:** Tatsächlichen Claude Memory Cleanup durchführen
   - Dateien löschen (via memory_delete tool)
   - CLAUDE.md aktualisieren

---

## SENSITIVE DATA ⚠️

Die Dateien in `integrations/` enthalten API-Credentials:
- `sipgate-oauth2-credentials.md` → Sipgate OAuth2 Client ID + Secret
- `twilio-credentials.md` → Twilio API Key + Auth Token

**Behandlung:**
- Nur in **private** GitHub-Repos speichern
- Niemals in Public-Repos pushen
- Lokal mit `git update-index --assume-unchanged` schützen
- Vor dem Push: `git status` prüfen

---

## Wo sind die echten Inhalte?

**Momentan:**
- Im Claude Memory Store (nicht exportierbar via API)
- Im Kontext-Fenster des Chats (Session 2026-09-19 16:01–17:49)
- Im Transcript: `/mnt/transcripts/2026-09-19-16-01-22-claude-memory-cleanup-repo.txt`

**Nach Export:**
- Hier in `memory-backup/` (strukturiert, versioniert)
- Im GitHub-Repo (Backup, History)
- Optional: im wbgrds/KaI Repo (Single Source of Truth)

---

## Weitere Informationen

- `MEMORY-MANIFEST.json` — Komplette Metadaten + Status aller 40 Dateien
- `MEMORY-CLEANUP-PLAN_2026-09-19.md` — Analyse & Keep/Delete-Listen
- `CLEANUP-CHECKLIST.md` — Abhakbare Checkliste für jede Datei

---

**Erstellt:** 2026-09-19T17:49:00Z  
**Olaf, Scharfenberg / WEBGUARDS UG**
