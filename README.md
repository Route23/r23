# Route23 release channel

Public download + auto-updater channel for **Route23** (source is private).

- `Route23.app.tar.gz` + `.sig` — updater artifacts (minisign-signed)
- `latest.json` — Tauri updater manifest (endpoint: `releases/latest/download/latest.json`)
- `*.dmg` — manual download

See the app's in-app updater (Settings → About). Design: ADR-0025.

## macOS — 初回起動 / First launch

このアプリは未署名のため、ダウンロード後の初回起動で macOS が **「"Route23" は壊れているため開けません」** と表示することがあります。ターミナルで次を実行してから開いてください（`.app` の場所は適宜変更）:

```
xattr -dr com.apple.quarantine /Applications/Route23.app
```

Because the app is unsigned, macOS may show **"Route23 is damaged and can't be opened"** the first time you open it after downloading. Run the command above (adjust the path), then open it. **Subsequent in-app auto-updates are unaffected.**
