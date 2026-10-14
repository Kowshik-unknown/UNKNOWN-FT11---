 Offlinerupee

Offlinerupee is a wallet **prototype** for demonstrating member sign-in, sandbox balances, peer-to-peer transfers, and a local offline-payment queue. It does not connect to banks or move real money.

| Mode | Services | Intended use |
| --- | --- | --- |
| Hosted demo | Firebase Authentication, Firestore, Firebase Hosting | Public sandbox demo on Firebase Spark |
| Local prototype | FastAPI, SQLite, browser local storage | Development and local-only test accounts |

The hosted Firebase demo does not depend on Render or Cloud Functions. Do not use this prototype to store or transfer real funds.

## Hosted demo

Try the hosted demo at [offline-rupee.web.app](https://offline-rupee.web.app). It uses Firebase Authentication and Firestore for demo accounts, profiles, and transfers. New accounts start with ₹5,000 in simulated funds. Firebase rules restrict access to wallet and transfer data; transfers are for demonstration only and do not move real money. The hosted demo does not use a transfer PIN.

## Local prototype

Local mode uses a separate SQLite database and does not use Firebase. From the repository root:

### Windows PowerShell

```powershell
py -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r backend\requirements.txt
.\.venv\Scripts\python.exe -m uvicorn backend.main:app --reload --host 127.0.0.1 --port 8000
```
