## 📦 `ailinux-server/README.md`

```markdown
# 🧠 AILinux Server Backup

Dieses Repository enthält vollständige **Backups des AILinux-Servers**, inklusive Mailserver, WordPress, Repo-Konfigurationen, AI-Komponenten und aller systemrelevanten Daten.

## 📦 Enthaltene Inhalte

- `/root/ailinux-repo/` – Mirror-Skripte, Signaturen, Dockerfiles, Konfiguration
- `/root/mailserver/` – Postfix, Dovecot, Spamfilter, SSL
- `/root/wordpress/` – Webseite mit bbPress, Nova Plugin, SEO Tools
- `/root/trainingsdaten/` – Lokale AI-Trainingsdaten für Nova/Ollama
- `/opt/nova-crawler/`, `/opt/nova-knowledge/`, `/opt/ollama/` – KI-Tools
- `/etc/systemd/system/` – Eigene systemd Dienste
- `~/.ollama/`, `~/backup.sh`, `~/.pat_git` – Lokale Tools & Konfig

## 🗃 Speicherorte

- 🔄 Backups: `/root/backups/`
- 📤 Git Push: `/root/ailinux-server-git/`
- 🔒 GitHub Remote: [`derleiti/ailinux-server`](https://github.com/derleiti/ailinux-server)

## 🚀 Backup starten

```bash
./backup.sh
Wähle anschließend, ob du das Backup direkt via Git LFS pushen oder nur lokal speichern möchtest.

🧠 Git LFS aktiviert
.zip-Dateien werden per Git LFS gespeichert, um große Backups (>100MB) zu verwalten.

🔐 Sicherheit
GitHub Personal Access Token wird aus ~/.pat_git geladen:

bash
Kopieren
Bearbeiten
echo 'export GITHUB_PAT=ghp_xxx' > ~/.pat_git
chmod 600 ~/.pat_git
⚙️ Automatisierung
Optional kann das Backup-Skript in einen systemd-Timer eingebunden werden, z. B. für tägliche Sicherung.

💬 Kontakt
Maintained by Markus Leitermann & Nova AI 🤝
https://derleiti.de · https://ailinux.me
