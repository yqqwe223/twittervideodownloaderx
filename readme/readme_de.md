# 🐦 X.com Video-Analyse-Tool

> Ein leichtes, schnelles und vielseitiges Werkzeug zum Extrahieren von Videoinhalten von X (ehemals Twitter)

[🌐 Online-Demo](https://twittervideodownloaderx.com/ge) • [📝 Bedienungsanleitung](#-bedienungsanleitung) • [❓ Häufig gestellte Fragen](#-häufig-gestellte-fragen)

---

## 📋 Projektübersicht

Dieses Projekt ist ein webbasiertes Analyse-Tool, das es ermöglicht, Videoressourcen aus öffentlichen Beiträgen auf X.com (ehemals Twitter) sicher zu extrahieren und in verschiedenen Formaten zu konvertieren und herunterzuladen. Keine Installation von Client-Software erforderlich, keine Konto-Registrierung nötig – nutzen Sie das Tool direkt über Ihren Browser.

> ⚠️ **Wichtiger Hinweis**: Dieses Tool dient ausschließlich persönlichen Lernzwecken, technischer Forschung und der Nutzung im Rahmen einer angemessenen Verwendung. Bitte halten Sie sich an die [Entwicklervereinbarung der X-Plattform](https://developer.twitter.com/en/developer-terms/agreement) sowie die Urheberrechtsgesetze Ihres Landes. Die Nutzung zu Zwecken, die Rechte Dritter verletzen, ist strengstens untersagt.

---

## ✨ Hauptfunktionen

- 🔗 **Link-Analyse**: Unterstützt standardmäßige X.com-Beitrags-URLs; automatische Erkennung von Videos und animierten GIFs
- 📥 **Export in mehreren Formaten**:
  - MP4-Video in Originalqualität
  - Audio-Extraktion → MP3-Format
  - Videoclip → Konvertierung zu animiertem GIF
- 🌍 **Mehrsprachige Oberfläche**: Unterstützung für Deutsch, Englisch, Chinesisch, Japanisch, Koreanisch und insgesamt 16 Sprachen
- 📱 **Plattformübergreifende Kompatibilität**: Funktioniert einwandfrei auf Chrome / Firefox / Safari / Edge; optimierte Erfahrung für Mobilgeräte und Tablets
- 🔒 **Datenschutz priorisiert**: Keine Konto-Registrierung erforderlich, keine Erfassung personenbezogener Daten; Analyseprozess vollständig anonym
- ⚡ **Schnelle Verarbeitung**: Analyse im Durchschnitt in unter 5 Sekunden abgeschlossen; Unterstützung für parallele Anfragen

---

## 🚀 Schnellstart

### Online-Nutzung (empfohlen)
1. Besuchen Sie [https://twittervideodownloaderx.com/ge](https://twittervideodownloaderx.com/ge)
2. Kopieren Sie den Link des Zielbeitrags (Beispiel: `https://x.com/user/status/123456789`)
3. Fügen Sie den Link in das Eingabefeld ein → Klicken Sie auf die Schaltfläche 「Analysieren」
4. Wählen Sie das gewünschte Format → Speichern Sie die Datei gemäß den Anweisungen Ihres Browsers

### Lokale Bereitstellung (für Entwickler)
```bash
# Repository klonen
git clone https://github.com/your-repo/x-video-parser.git

# Abhängigkeiten installieren
cd x-video-parser && npm install

# Umgebungsvariablen konfigurieren (optional)
cp .env.example .env

# Entwicklungsserver starten
npm run dev
```

> 💡 Hinweis: Dieses Projekt verwendet eine Architektur basierend auf Node.js + Express. Detaillierte Bereitstellungsinformationen finden Sie in `/docs/DEPLOY.md`

---

## 🛠 Technologie-Stack

| Modul | Eingesetzte Technologien |
|-------|--------------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Videoverarbeitung | ffmpeg.wasm (leichtgewichtige Frontend-Konvertierung) |
| Proxy-Weiterleitung | Cloudflare Workers / Benutzerdefinierte Middleware |
| Internationalisierung | vue-i18n + JSON-Sprachpakete |

---

## 📚 Bedienungsanleitung

### Grundlegender Arbeitsablauf
```
1. Link des Beitrags erhalten
   └─ Öffnen Sie den Zielbeitrag auf X.com → Kopieren Sie die URL aus der Adressleiste des Browsers

2. Analyse-Anfrage senden
   └─ Fügen Sie den Link in das Eingabefeld des Tools ein → Klicken Sie auf 「Video herunterladen」

3. Ausgabeformat auswählen
   ├─ 🎬 Als MP4 herunterladen: Mit Originalqualität speichern
   ├─ 🎵 In MP3 konvertieren: Audio-Spur extrahieren
   └─ 🎞 In GIF konvertieren: Kurze Animation erstellen (empfohlen: ≤15 Sekunden)

4. Datei speichern
   └─ Die Ressource wird in einem neuen Tab geöffnet → Rechtsklick/Menü → 「Speichern unter」
```

### Tipps für die Nutzung auf Mobilgeräten
- iOS Safari: Schaltfläche „Teilen" → 「In Dateien speichern」
- Android Chrome: Video lange drücken → 「Video herunterladen」
- Bei automatischer Wiedergabe: Klicken Sie auf `⋮` oben rechts im Player → Wählen Sie 「Herunterladen」

---

## ❓ Häufig gestellte Fragen

**F: Wo werden heruntergeladene Dateien gespeichert?**  
A: Dateien werden im im Browser konfigurierten Download-Ordner gespeichert. Sie können diesen Pfad in den Browsereinstellungen überprüfen oder ändern.

**F: Kann ich private Konten oder eingeschränkte Inhalte analysieren?**  
A: Nein. Dieses Tool funktioniert nur mit öffentlich eingestellten Beiträgen und respektiert die Zugriffseinstellungen des Originalinhalts.

**F: Wird die Bild-/Tonqualität nach der Konvertierung reduziert?**  
A: Das MP4-Format behält die Originalqualität bei. Das MP3-Format verwendet eine Standardkodierung mit 128 kbps. Das GIF-Format optimiert die Bildrate entsprechend der Dauer, um ein Gleichgewicht zwischen Dateigröße und Flüssigkeit zu erreichen.

**F: Wird der Download-Verlauf oder Cache gespeichert?**  
A: Nein. Alle Ressourcen werden direkt über einen temporären Proxy an das Gerät des Nutzers übertragen; der Server speichert keine Anfragen oder Mediendateien.

**F: Was tun, wenn die Analyse fehlschlägt?**  
A: Bitte überprüfen Sie: ① Ob der Link zu einem gültigen öffentlichen Beitrag führt ② Ob Ihre Internetverbindung stabil ist ③ Versuchen Sie es mit einem anderen Browser. Bei fortbestehenden Problemen melden Sie dies bitte über ein Issue.

---

## ⚖️ Einhaltung von Vorschriften und Haftungsausschluss

- Dieses Tool **umgeht oder verletzt keine technischen Schutzmaßnahmen** von Plattformen; es ruft lediglich Metadaten über öffentliche Schnittstellen ab
- Der Nutzer ist selbst dafür verantwortlich, sicherzustellen, dass seine Nutzung den örtlichen Gesetzen und den Nutzungsbedingungen der Plattform entspricht
- Empfohlene Anwendungsfälle: Persönliche Archivierung, Bildungspräsentationen, Referenzmaterial für die Inhaltserstellung... stets im Rahmen der zulässigen Nutzung (Fair Use)
- Wenn Sie Inhalte entdecken, die möglicherweise Rechte verletzen, wenden Sie sich bitte über [dieses Urheberrechts-Meldeformular von X](https://help.twitter.com/forms/dmca) an den offiziellen Kanal

---

## 🤝 Leitfaden für Beiträge

Wir freuen uns über Ihre Pull Requests und Issue-Meldungen! Vor dem Beitragen bitten wir Sie, Folgendes zu lesen:
- [Code-Standards](/CONTRIBUTING.md)
- [Mehrsprachiger Übersetzungsleitfaden](/locales/README.md)
- [Sicherheits- und Compliance-Anforderungen](/SECURITY.md)

---

## 📄 Lizenz

Dieses Projekt wird unter der [MIT-Lizenz](/LICENSE) veröffentlicht. Es kann kostenlos für Bildungs- und Forschungszwecke genutzt werden. Bei kommerzieller Nutzung prüfen Sie bitte sorgfältig die Einhaltung der geltenden rechtlichen Vorschriften.

---

> 🌟 Wenn Ihnen dieses Tool hilfreich war, würden wir uns sehr über ✨einen Stern (Star) freuen! Ihre Unterstützung ist die größte Motivation für uns, dieses Projekt weiterhin zu pflegen und zu verbessern~

*Zuletzt aktualisiert: Mai 2026 | Version: v2.1.0*