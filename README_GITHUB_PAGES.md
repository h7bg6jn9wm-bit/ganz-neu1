# SHK Theorie Trainer – GitHub Pages + Backend

## 1. Frontend auf GitHub Pages
Lade **nur den Inhalt dieses Ordners** in dein GitHub-Repository hoch.

Wichtig: In `api-config.js` muss `window.SHK_API_BASE` auf die echte Backend-Adresse zeigen, z. B.:

```js
window.SHK_API_BASE = "https://api.shk-trainer.de";
```

Danach GitHub → Settings → Pages → Deploy from branch → `main` → `/ (root)`.

## 2. Backend
Das Backend im Ordner `../backend` läuft auf deinem VPS. Setze dort in `.env` mindestens:

- `DATABASE_URL`
- `POSTGRES_PASSWORD`
- `COOKIE_SECURE=true`
- `TRUST_PROXY=true`
- `FRONTEND_ORIGIN=https://app.shk-trainer.de`

## 3. Empfohlene Domain-Struktur
Für sichere Cookie-Sessions empfehle ich:

- Web-App: `https://app.shk-trainer.de`
- API: `https://api.shk-trainer.de`

Beide liegen damit unter derselben Hauptdomain.

## 4. Wichtig
`.env`, echte Passwörter, Datenbank-Credentials und private Schlüssel **niemals** in GitHub hochladen.
