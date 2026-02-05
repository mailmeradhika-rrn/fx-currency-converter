# Automated FX Currency Converter 💱

### **The Problem**
In global operations, manual FX conversions for cross-border transactions are prone to human error, leading to reconciliation discrepancies and operational delays. Business users often need a quick, accurate way to convert amounts without manually searching for rates or using unverified calculators.

### **The Solution & Business Logic**
I architected an automated workflow using **n8n** that serves as a bridge between user-submitted data and real-time financial markets. 

**The specific business logic includes:**
1.  **Data Capture:** Utilizing a **Tally.so** form to capture structured user input (Base Currency, Amount, and Target Currency) which is pushed to the workflow via a **Webhook**.
2.  **Market Calibration:** The workflow calls a **Financial API** to fetch live mid-market exchange rates, ensuring the conversion is based on current market conditions.
3.  **Conversion Engine:** Dynamically calculating the target amount based on the real-time currency pair and the user-provided volume.
4.  **Automated Notification:** Executing a logic-gate to trigger an immediate **Email Notification** to the user, delivering the final calculated figures in a professional, structured format.

---

## 🛠️ Tech Stack
- **Orchestration:** n8n
- **Intake:** Tally.so (via Webhooks)
- **Data Source:** Financial Exchange Rate APIs
- **Communication:** Gmail/SMTP Node
- **Data Format:** JSON / Webhook Payloads

---

## 🚀 Impact
- **Accuracy:** Eliminated 100% of manual calculation errors.
- **Efficiency:** Transitioned a manual lookup process into an instantaneous automated response.
- **User Experience:** Provides a clean, form-based interface for users to interact with complex backend logic.

---

## 📂 Files in this Repo
- `Forex Calculator.json`: The full n8n workflow export.
