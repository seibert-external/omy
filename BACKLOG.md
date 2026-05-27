# Ωmy – Backlog

## Offen

### People Directory Integration
Teilnehmende direkt aus einem Seibert People Directory wählen.
- Personen per Name/Rolle suchen und zur Abstimmung einladen
- Tracking: wer hat abgestimmt, wer noch nicht
- Reminder an ausstehende Personen
- Aktuell: Abstimmung läuft offen, jede Person mit Link kann abstimmen

### SSO / Google Workspace Login
Abstimmung nur für eingeloggte Seibert-Accounts zugänglich.
- Verhindert Mehrfachabstimmungen unter falschen Namen
- Voraussetzung für People Directory Integration

### Confluence Auto-Export
Entscheidungen automatisch als Confluence-Seite dokumentieren.
- Aktuell: Markdown-Export (manuell)

### Asynchrone Benachrichtigung
E-Mail oder Google Chat Notification wenn neue Abstimmung gestartet wird.

### Mehr als 2 Runden
Aktuell: max. Runde 2 → Meeting. Ggf. konfigurierbar machen.

### Apps Script LockService (serverseitiger Schreibschutz)
Aktuell wird Race Condition beim gleichzeitigen Schreiben clientseitig per Debounce abgefangen. Für Weg B (oder bei echtem Mehrbenutzerbetrieb) sollte `doPost()` im Apps Script mit `LockService.getScriptLock()` abgesichert werden, damit parallele Schreibvorgänge serialisiert werden und keine Duplikat-Zeilen entstehen.

### Rollenkonzept
Klare Trennung von Rollen mit unterschiedlichen Rechten:
- **Ersteller*in** – legt Entscheidung an
- **Moderator*in** – steuert den Prozess (Runden schließen/öffnen, Runde 2 starten)
- **Abstimmer*in** – gibt Widerstand und Kommentar ab
- Aktuell: alle Rollen sind offen, kein Zugriffsschutz zwischen ihnen
