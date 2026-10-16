# India-Stocks-1231-1260-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1231 to 1260)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1231-1260-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1231 to 1260)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1231 | `HATHWAY` | Hathway Cable & Datacom Limited | `HATHWAY.NS` |
| 1232 | `HATSUN` | Hatsun Agro Product Limited | `HATSUN.NS` |
| 1233 | `HAVISHA` | Sri Havisha Hospitality and Infrastructure Limited | `HAVISHA.NS` |
| 1234 | `HAWKINCOOK` | Hawkins Cookers Limited | `HAWKINCOOK.NS` |
| 1235 | `HAZOOR` | Hazoor Multi Projects Limited | `HAZOOR.NS` |
| 1236 | `HBESD` | HB Estate Developers Limited | `HBESD.NS` |
| 1237 | `HBPOR` | HB Portfolio Limited | `HBPOR.NS` |
| 1238 | `HBSL` | HB Stockholdings Limited | `HBSL.NS` |
| 1239 | `HCC` | Hindustan Construction Company Limited | `HCC.NS` |
| 1240 | `HCG` | Healthcare Global Enterprises Limited | `HCG.NS` |
| 1241 | `HCL-INSYS` | HCL Infosystems Limited | `HCL-INSYS.NS` |
| 1242 | `HDIL` | Housing Development and Infrastructure Limited | `HDIL.NS` |
| 1243 | `HEADSUP` | Heads UP Ventures Limited | `HEADSUP.NS` |
| 1244 | `HEALTHX` | Health X Platform Limited | `HEALTHX.NS` |
| 1245 | `HECPROJECT` | HEC Infra Projects Limited | `HECPROJECT.NS` |
| 1246 | `HEIDELBERG` | HeidelbergCement India Limited | `HEIDELBERG.NS` |
| 1247 | `HEMIPROP` | Hemisphere Properties India Limited | `HEMIPROP.NS` |
| 1248 | `HERANBA` | Heranba Industries Limited | `HERANBA.NS` |
| 1249 | `HERITGFOOD` | Heritage Foods Limited | `HERITGFOOD.NS` |
| 1250 | `HEROMOTORS` | Hero Motors Limited | `HEROMOTORS.NS` |
| 1251 | `HESTERBIO` | Hester Biosciences Limited | `HESTERBIO.NS` |
| 1252 | `HEXAGON` | Hexagon Nutrition Limited | `HEXAGON.NS` |
| 1253 | `HEXATRADEX` | Hexa Tradex Limited | `HEXATRADEX.NS` |
| 1254 | `HGINFRA` | H.G. Infra Engineering Limited | `HGINFRA.NS` |
| 1255 | `HGM` | HandsOn Global Management (HGM) Limited | `HGM.NS` |
| 1256 | `HGS` | Hinduja Global Solutions Limited | `HGS.NS` |
| 1257 | `HIKAL` | Hikal Limited | `HIKAL.NS` |
| 1258 | `HILINFRA` | Highway Infrastructure Limited | `HILINFRA.NS` |
| 1259 | `HILTON` | Hilton Metal Forging Limited | `HILTON.NS` |
| 1260 | `HIMATSEIDE` | Himatsingka Seide Limited | `HIMATSEIDE.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream HATHWAY 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1231-1260-Historical-Data/main/HATHWAY/1m/2026/10/HATHWAY_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
