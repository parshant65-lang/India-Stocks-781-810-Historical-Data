# India-Stocks-781-810-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 781 to 810)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-781-810-Historical-Data/
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

## 📦 Constituents (781 to 810)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 781 | `BHARATRAS` | Bharat Rasayan Limited | `BHARATRAS.NS` |
| 782 | `BHARATSE` | Bharat Seats Limited | `BHARATSE.NS` |
| 783 | `BHARATWIRE` | Bharat Wire Ropes Limited | `BHARATWIRE.NS` |
| 784 | `BI` | Bilcare Limited | `BI.NS` |
| 785 | `BIGBLOC` | Bigbloc Construction Limited | `BIGBLOC.NS` |
| 786 | `BIKAJI` | Bikaji Foods International Limited | `BIKAJI.NS` |
| 787 | `BIL` | Bhartiya International Limited | `BIL.NS` |
| 788 | `BILVYAPAR` | BIL VYAPAR LIMITED | `BILVYAPAR.NS` |
| 789 | `BIMETAL` | Bimetal Bearings Limited | `BIMETAL.NS` |
| 790 | `BIOFILCHEM` | Biofil Chemicals & Pharmaceuticals Limited | `BIOFILCHEM.NS` |
| 791 | `BIRLACABLE` | Birla Cable Limited | `BIRLACABLE.NS` |
| 792 | `BIRLACORPN` | Birla Corporation Limited | `BIRLACORPN.NS` |
| 793 | `BIRLAMONEY` | Aditya Birla Money Limited | `BIRLAMONEY.NS` |
| 794 | `BIRLANU` | BirlaNu Limited | `BIRLANU.NS` |
| 795 | `BIRLAPREC` | Birla Precision Technologies Limited | `BIRLAPREC.NS` |
| 796 | `BLACKBUCK` | BLACKBUCK LIMITED | `BLACKBUCK.NS` |
| 797 | `BLACKROSE` | Black Rose Inds. Limited | `BLACKROSE.NS` |
| 798 | `BLAL` | BEML Land Assets Limited | `BLAL.NS` |
| 799 | `BLBLIMITED` | BLB Limited | `BLBLIMITED.NS` |
| 800 | `BLEL` | Behari Lal Engineering Limited | `BLEL.NS` |
| 801 | `BLIL` | Balmer Lawrie Investments Limited | `BLIL.NS` |
| 802 | `BLISSGVS` | Bliss GVS Pharma Limited | `BLISSGVS.NS` |
| 803 | `BLKASHYAP` | B. L. Kashyap and Sons Limited | `BLKASHYAP.NS` |
| 804 | `BLSE` | BLS E-Services Limited | `BLSE.NS` |
| 805 | `BLUECHIP` | Blue Chip India Limited | `BLUECHIP.NS` |
| 806 | `BLUECLOUDS` | Blue Cloud Softech Solutions Limited | `BLUECLOUDS.NS` |
| 807 | `BLUECOAST` | Blue Coast Hotels Limited | `BLUECOAST.NS` |
| 808 | `BLUEDART` | Blue Dart Express Limited | `BLUEDART.NS` |
| 809 | `BLUEJET` | Blue Jet Healthcare Limited | `BLUEJET.NS` |
| 810 | `BLUESTONE` | BlueStone Jewellery and Lifestyle Limited | `BLUESTONE.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream BHARATRAS 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-781-810-Historical-Data/main/BHARATRAS/1m/2026/10/BHARATRAS_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
