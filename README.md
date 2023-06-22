# sheets-example
A google sheets Meltano example

[Get yourself a refresh token](https://medium.com/@aaron.phethean/google-oauth-refresh-tokens-are-a-total-pain-d7d98c8fa7f8)

This project was created with commands similar to this:
```
meltano init sheets-example
cd sheets-example
meltano add extractor tap-google-sheets
```

To export your sheet data you need to install, set the environment, and run

Install

```
git clone [this repo]
meltano install
```

Create a .env

```
TAP_GOOGLE_SHEETS_OAUTH_CREDENTIALS_CLIENT_ID=[PUT YOUR CLIENT ID HERE]
TAP_GOOGLE_SHEETS_OAUTH_CREDENTIALS_CLIENT_SECRET=[PUT YOUR CLIENT SECRET HERE]
TAP_GOOGLE_SHEETS_OAUTH_CREDENTIALS_SCOPE=https://www.googleapis.com/auth/spreadsheets.readonly https://www.googleapis.com/auth/drive.readonly
TAP_GOOGLE_SHEETS_OAUTH_CREDENTIALS_REFRESH_TOKEN=[PUT YOUR REFRESH TOKEN HERE]
TAP_GOOGLE_SHEETS_SHEET_ID=[PUT YOUR SHEET ID HERE]
TAP_GOOGLE_SHEETS_KEY_PROPERTIES=["name"]
MELTANO_ENVIRONMENT=dev
```

Run

```
meltano run tap-google-sheets target-jsonl
```
