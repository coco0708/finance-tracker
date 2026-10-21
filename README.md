# Finance Tracker

An Android app for tracking everyday money: cash and daily expenses, commodities (rice, LPG, fuel...),
insurance premiums, credit cards, loans and installments, and online shopping orders.

- `web/app.html` - the app itself (edit this)
- `build_web.py` - copies the app into the Android project (`python build_web.py`) and makes a browser preview in `preview/`
- `android/` - the Android project (a WebView that saves your data to a private file on the phone)
- `.github/workflows/build-apk.yml` - builds the APK on GitHub and posts it under Releases

## What it tracks

| Area | What you get |
| --- | --- |
| Daily expenses | Expenses, income and transfers across cash, bank, e-wallet and card accounts; monthly budget and per-category limits; today's spend and a per-day allowance |
| Commodities | Switch on "Track quantity and unit price" on any expense; see the unit price, change vs. last purchase, average, low/high and a price chart per item |
| Insurance | Policies with premium, frequency, coverage and expiry; "Pay premium" records the expense and moves the next due date |
| Credit cards | Balance owed, limit and utilisation, statement balance and due date from your statement/due days; "Pay card" records a transfer from your bank |
| Loans | Money you owe (bank, salary, car, housing, government, card installments) and money owed to you; payments made, remaining, next due and last-payment date |
| Online shopping | Orders by shop, payment method and status; card/e-wallet orders count as spending right away, COD when received; cancellations and refunds |

The Home screen pulls it together: spending vs. budget, what's due in the next 3 weeks, where the money went, the last 6 months, and your net worth.

## Get the APK with GitHub

1. On github.com create an empty repository named `finance-tracker` (no README).
2. Push this folder (see the PowerShell commands you were given).
3. Open the repository's **Actions** tab and wait for "Build APK" to finish (about 3-5 minutes).
4. On your phone open `https://github.com/coco0708/finance-tracker/releases`, download `FinanceTracker.apk` and open it.

Every push to `main` builds a new APK. It is signed with the same key every time (`android/app/finance-tracker.jks`),
so installing a new version keeps your data.

## Backups

Accounts → Your data → **Save backup** writes a `.json` file wherever you choose (Downloads, Drive).
**Restore backup** reads it back. **Share as CSV** sends all transactions to a spreadsheet app.
