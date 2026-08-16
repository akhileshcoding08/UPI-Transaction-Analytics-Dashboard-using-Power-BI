# UPI Transaction Analytics Dashboard

An end-to-end analytics project that explores 250,000 UPI (Unified Payments Interface) transactions from 2024 and presents the findings through an interactive Power BI dashboard covering executive KPIs, merchant behaviour, geography, banking/technology trends, and fraud risk.

![Platform](https://img.shields.io/badge/Platform-Power%20BI-F2C811?logo=powerbi&logoColor=black)
![Data](https://img.shields.io/badge/Data-250K%20records-blue)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## Project Overview

UPI is India's real-time payment system, and understanding transaction patterns is critical for banks, fintech companies, and regulators. This project analyzes a full year (Jan–Dec 2024) of simulated UPI transaction data to uncover:

- Overall transaction volume, value, and success/failure trends
- How different merchant categories and transaction types behave
- Geographic and demographic spending patterns across Indian states and age groups
- Bank- and technology-level performance (device type, network type)
- Fraud indicators and risk hotspots

The final deliverable is a 5-page interactive Power BI dashboard (`UPI_Transaction_Analytics_Dashboard.pbix`).

## Dataset

**File:** `upi_transactions_2024.csv`

| Detail | Value |
|---|---|
| Records | 250,000 transactions |
| Time period | Jan 1, 2024 – Dec 30, 2024 |
| Columns | 17 |
| Transaction types | P2P, P2M, Bill Payment, Recharge |
| States covered | 10 |
| Merchant categories | 10 |
| Banks | 8 |

**Columns:**

| Column | Description |
|---|---|
| `transaction id` | Unique transaction identifier |
| `timestamp` | Date and time of transaction |
| `transaction type` | P2P, P2M, Bill Payment, or Recharge |
| `merchant_category` | Category of merchant (Grocery, Fuel, Entertainment, etc.) |
| `amount (INR)` | Transaction amount in Indian Rupees |
| `transaction_status` | SUCCESS or FAILED |
| `sender_age_group` / `receiver_age_group` | Age bracket of sender/receiver |
| `sender_state` | Indian state of the sender |
| `sender_bank` / `receiver_bank` | Bank involved in the transaction |
| `device_type` | Android, iOS, or Web |
| `network_type` | 3G, 4G, 5G, or WiFi |
| `fraud_flag` | 1 if flagged fraudulent, else 0 |
| `hour_of_day` | Hour the transaction occurred (0–23) |
| `day_of_week` | Day name |
| `is_weekend` | 1 if weekend, else 0 |

## Dashboard Pages

The Power BI file contains 5 report pages:

1. **Executive Overview** – headline KPIs (total transactions, total value, success rate), trend line over time, transaction type split, and a state-wise map
2. **Transaction & Merchant Analysis** – merchant category performance, transaction type breakdown, and trends over time
3. **Geographic & Demographic Analysis** – state-wise map, age-group behaviour, and comparisons across regions
4. **Banking and Technology Analysis** – bank-wise performance, device type (Android/iOS/Web), and network type (3G/4G/5G/WiFi) breakdown
5. **Fraud & Risk Monitoring** – fraud KPIs, fraud trends over time, and category/state-level risk breakdown

## Tools Used

- **Power BI Desktop** – data modeling, DAX measures, and dashboard/report design
- **Power Query** – data cleaning and transformation
- **CSV / Excel** – raw data source

## Repository Structure

```
upi-transaction-analytics-dashboard/
│
├── UPI_Transaction_Analytics_Dashboard.pbix   # Power BI dashboard file
├── upi_transactions_2024.csv                  # Source dataset
├── README.md                                  # Project documentation (this file)
└── docs/
    └── UPI_Transaction_Analytics_Project_Documentation.docx   # Full step-by-step project documentation
```

## How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/upi-transaction-analytics-dashboard.git
   ```
2. Open `UPI_Transaction_Analytics_Dashboard.pbix` in **Power BI Desktop** (free download from Microsoft).
3. If prompted to locate the data source, point it to `upi_transactions_2024.csv` in the cloned folder.
4. Use the slicers on each page to filter by date, state, transaction type, bank, or merchant category.

## Key Insights

- Out of 250,000 transactions, **237,624 (≈95.1%)** succeeded and **12,376 (≈4.9%)** failed.
- **480 transactions (≈0.19%)** were flagged as fraudulent.
- Total transaction value across the dataset is approximately **₹32.79 crore**.
- **P2P (person-to-person)** transfers are the most common transaction type, followed by **P2M (person-to-merchant)** payments.
- **Android** is the dominant device type, followed by iOS and Web.
- **4G** is the most-used network type, ahead of 5G, WiFi, and 3G.

## Full Documentation

For a detailed, step-by-step walkthrough of how this project was built from data understanding through Power BI modeling, DAX measures, dashboard design, and GitHub publishing — see:

📄 [`docs/UPI_Transaction_Analytics_Project_Documentation.docx`](docs/UPI_Transaction_Analytics_Project_Documentation.docx)

## Author

Feel free to connect or raise an issue if you have suggestions or questions about this project.

**Akhilesh** — [GitHub](https://github.com/akhileshcoding08)
