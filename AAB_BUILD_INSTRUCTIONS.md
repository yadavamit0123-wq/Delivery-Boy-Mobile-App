# Delivery Boy — Play Store AAB (GitHub Actions)

App ID: `com.pt.palviagricodelivery`  
Version in `pubspec.yaml`: `1.0.2+3` → versionName `1.0.2`, versionCode `3`

## 1) GitHub Secrets

Repo: https://github.com/yadavamit0123-wq/Delivery-Boy-Mobile-App  
**Settings → Secrets and variables → Actions → New repository secret**

| Secret | Value |
|---|---|
| `KEYSTORE_BASE64` | keystore base64 (command below) |
| `KEYSTORE_PASSWORD` | keystore password |
| `KEY_ALIAS` | key alias |
| `KEY_PASSWORD` | key password |

Mac:

```bash
base64 -i /Users/amityadav/Downloads/prt.jks | pbcopy
```

(Agar Delivery Boy ke liye alag `.jks` hai to usi path use karo.)

## 2) Build AAB

1. Push code to `main` (workflow + signing config).
2. **Actions → Build Release AAB → Run workflow**
3. Artifacts → `release-aab` → download → `app-release.aab`
4. Upload to Play Console.

## Notes

- Never commit `.jks` / passwords.
- Play Store needs this app’s correct upload keystore (same as previous Play uploads if app already exists).
