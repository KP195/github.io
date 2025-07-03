# Deployment-Anleitung für Ihren Jekyll Blog

Diese Anleitung führt Sie Schritt für Schritt durch die Einrichtung und das Deployment Ihres Jekyll-Blogs auf GitHub Pages.

## Voraussetzungen

- Ein GitHub-Account
- Grundkenntnisse in Git (optional, aber hilfreich)
- Einen Texteditor (VS Code, Sublime Text, oder sogar der GitHub Web-Editor)

## Schritt 1: Repository erstellen

### 1.1 Neues Repository auf GitHub erstellen
1. Loggen Sie sich in GitHub ein
2. Klicken Sie auf "New Repository" (grüner Button)
3. **Wichtig:** Nennen Sie das Repository `ihrbenutzername.github.io`
   - Ersetzen Sie "ihrbenutzername" durch Ihren tatsächlichen GitHub-Benutzernamen
   - Beispiel: Wenn Ihr Benutzername "max-mustermann" ist, nennen Sie es `max-mustermann.github.io`
4. Stellen Sie sicher, dass das Repository **Public** ist
5. Aktivieren Sie "Add a README file"
6. Klicken Sie auf "Create repository"

### 1.2 Warum dieser spezielle Name?
GitHub erkennt automatisch Repositories mit dem Namen `benutzername.github.io` als GitHub Pages Sites und aktiviert das Hosting automatisch.

## Schritt 2: Jekyll-Dateien hinzufügen

### 2.1 Dateien über den GitHub Web-Editor hinzufügen
Sie können alle Dateien direkt im Browser über GitHub hinzufügen:

1. Gehen Sie zu Ihrem Repository
2. Klicken Sie auf "Add file" → "Create new file"
3. Erstellen Sie nacheinander alle Dateien aus diesem Guide

### 2.2 Dateien über Git hinzufügen (für Fortgeschrittene)
```bash
# Repository klonen
git clone https://github.com/ihrbenutzername/ihrbenutzername.github.io.git
cd ihrbenutzername.github.io

# Dateien hinzufügen (siehe unten)
# ...

# Änderungen committen
git add .
git commit -m "Initial Jekyll setup"
git push origin main
```

### 2.3 Reihenfolge der zu erstellenden Dateien
Erstellen Sie die Dateien in dieser Reihenfolge:

1. `_config.yml` (Konfiguration)
2. `Gemfile` (Abhängigkeiten)
3. `index.html` (Startseite)
4. `about.md` (Über-Seite)
5. Ordner `_posts/` erstellen
6. `_posts/2024-07-02-mein-erster-blog-post.md` (Erster Artikel)
7. `_posts/2024-07-01-jekyll-github-pages-anleitung.md` (Zweiter Artikel)
8. Ordner `assets/css/` erstellen
9. `assets/css/style.scss` (Custom Styles)
10. Ordner `.github/workflows/` erstellen
11. `.github/workflows/pages.yml` (GitHub Actions)

## Schritt 3: Konfiguration anpassen

### 3.1 _config.yml bearbeiten
Öffnen Sie `_config.yml` und passen Sie folgende Werte an:

```yaml
title: "Ihr Blog-Name"                    # ← Ihren gewünschten Blog-Namen
description: "Ihre Blog-Beschreibung"     # ← Kurze Beschreibung Ihres Blogs
author: "Ihr vollständiger Name"          # ← Ihr Name
email: "ihre.email@example.com"          # ← Ihre E-Mail-Adresse
url: "https://ihrbenutzername.github.io" # ← Ihre GitHub Pages URL

github_username: ihrbenutzername         # ← Ihr GitHub-Benutzername
twitter_username: ihrtwitter             # ← Optional: Ihr Twitter-Handle
```

### 3.2 About-Seite personalisieren
Bearbeiten Sie `about.md` und ersetzen Sie die Platzhalter durch Ihre persönlichen Informationen.

## Schritt 4: GitHub Pages aktivieren

### 4.1 Automatische Aktivierung
Wenn Sie Ihr Repository korrekt benannt haben (`benutzername.github.io`), wird GitHub Pages automatisch aktiviert.

### 4.2 Manuelle Aktivierung (falls nötig)
1. Gehen Sie zu Ihrem Repository auf GitHub
2. Klicken Sie auf "Settings" (oben rechts)
3. Scrollen Sie zu "Pages" (linke Seitenleiste)
4. Unter "Source" wählen Sie "Deploy from a branch"
5. Wählen Sie "main" als Branch
6. Klicken Sie auf "Save"

### 4.3 GitHub Actions aktivieren
Die mitgelieferte `.github/workflows/pages.yml` Datei sorgt für automatisches Building. Stellen Sie sicher, dass GitHub Actions in Ihren Repository-Einstellungen aktiviert ist:

1. Gehen Sie zu "Settings" → "Actions" → "General"
2. Stellen Sie sicher, dass "Allow all actions and reusable workflows" ausgewählt ist

## Schritt 5: Ersten Deploy durchführen

### 5.1 Build-Prozess überwachen
1. Nachdem Sie alle Dateien hinzugefügt haben, gehen Sie zum "Actions" Tab Ihres Repositories
2. Sie sollten einen laufenden Workflow sehen
3. Klicken Sie darauf, um den Fortschritt zu verfolgen
4. Der Build dauert normalerweise 2-5 Minuten

### 5.2 Website besuchen
Sobald der Build erfolgreich abgeschlossen ist:
1. Ihre Website ist unter `https://ihrbenutzername.github.io` erreichbar
2. Es kann zusätzlich 5-10 Minuten dauern, bis die Änderungen global verfügbar sind

## Schritt 6: Ersten eigenen Blog-Post erstellen

### 6.1 Neuen Post erstellen
1. Gehen Sie in den `_posts/` Ordner
2. Erstellen Sie eine neue Datei mit dem Format: `YYYY-MM-DD-titel-des-posts.md`
3. Beispiel: `2024-07-03-mein-zweiter-post.md`

### 6.2 Front Matter hinzufügen
Jeder Post muss mit Front Matter beginnen:

```markdown
---
layout: post
title: "Titel Ihres Posts"
date: 2024-07-03 15:30:00 +0200
categories: [kategorie1, kategorie2]
tags: [tag1, tag2, tag3]
author: "Ihr Name"
excerpt: "Eine kurze Beschreibung des Posts für SEO und Vorschau."
---

Hier beginnt Ihr eigentlicher Post-Inhalt...
```

### 6.3 Markdown verwenden
Schreiben Sie Ihren Post in Markdown:

```markdown
# Überschrift 1
## Überschrift 2

Das ist ein normaler Paragraph mit **fettem Text** und *kursivem Text*.

- Listenpunkt 1
- Listenpunkt 2

[Link zu einer anderen Seite](https://example.com)

```code-block```
```

## Schritt 7: Lokale Entwicklung einrichten (Optional)

Für eine effizientere Entwicklung können Sie Jekyll lokal installieren:

### 7.1 Ruby installieren
- **Windows:** [RubyInstaller](https://rubyinstaller.org/)
- **macOS:** Ruby ist vorinstalliert, aber verwenden Sie besser [rbenv](https://github.com/rbenv/rbenv)
- **Linux:** `sudo apt-get install ruby-full` (Ubuntu/Debian)

### 7.2 Bundler installieren
```bash
gem install bundler
```

### 7.3 Abhängigkeiten installieren
```bash
cd ihrbenutzername.github.io
bundle install
```

### 7.4 Lokalen Server starten
```bash
bundle exec jekyll serve
```

Ihre Website ist dann unter `http://localhost:4000` erreichbar.

## Häufige Probleme und Lösungen

### Problem: Build schlägt fehl
**Lösung:**
1. Überprüfen Sie die GitHub Actions Logs
2. Stellen Sie sicher, dass alle Dateien gültiges Front Matter haben
3. Kontrollieren Sie die YAML-Syntax in `_config.yml`

### Problem: Website zeigt nur README
**Lösung:**
1. Stellen Sie sicher, dass Sie eine `index.html` oder `index.md` Datei haben
2. Überprüfen Sie, ob GitHub Pages aktiviert ist

### Problem: Styles werden nicht geladen
**Lösung:**
1. Kontrollieren Sie, dass `assets/css/style.scss` Front Matter hat (die --- Zeilen am Anfang)
2. Leeren Sie den Browser-Cache

### Problem: Posts erscheinen nicht
**Lösung:**
1. Überprüfen Sie das Dateinamen-Format: `YYYY-MM-DD-titel.md`
2. Stellen Sie sicher, dass das Datum nicht in der Zukunft liegt
3. Kontrollieren Sie das Front Matter Format

## Wartung und Updates

### Regelmäßige Aufgaben
1. **Abhängigkeiten aktualisieren:** Führen Sie gelegentlich `bundle update` aus (lokal)
2. **Backup:** Ihr Repository ist bereits Ihr Backup, aber exportieren Sie gelegentlich wichtige Inhalte
3. **Monitoring:** Überwachen Sie die GitHub Actions für fehlgeschlagene Builds

### Erweiterte Konfiguration
- Fügen Sie Google Analytics hinzu (über `_config.yml`)
- Installieren Sie zusätzliche Jekyll-Plugins
- Erstellen Sie eigene Layouts und Includes
- Implementieren Sie Kommentarsysteme (z.B. Disqus)

## Nächste Schritte

Nach erfolgreichem Deployment können Sie:
1. Das Design weiter anpassen
2. Weitere Seiten hinzufügen
3. Ein anderes Jekyll-Theme installieren
4. Zusätzliche Plugins für erweiterte Funktionen nutzen
5. Eine eigene Domain verwenden

## Support und Ressourcen

- [Jekyll Dokumentation](https://jekyllrb.com/docs/)
- [GitHub Pages Dokumentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)
- [Jekyll Community Forum](https://talk.jekyllrb.com/)

Bei spezifischen Problemen können Sie auch Issues in diesem Repository erstellen oder mich direkt kontaktieren.
