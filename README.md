<div align="center">
  <img src="https://n8n.io/favicon.ico" width="80" alt="n8n logo" />
  <h1>📈 Smart Lead Follow-Up Automation</h1>
  <p><strong>Automated multi-channel outreach, scoring, and follow-up system powered by n8n</strong></p>
</div>

---

## ⚡ Overview

**Smart Lead Follow-Up Automation** is a sophisticated n8n workflow designed to instantly handle incoming leads, score their quality based on available data, and trigger dynamic follow-up procedures.

By distinguishing between "Hot", "Warm", and "Cold" leads instantly, your sales team can prioritize high-value prospects immediately via WhatsApp, while letting automated systems nurture cooler leads over time.

## 🎯 When to Use It

This workflow is perfect for:
- **B2B Sales Teams:** Instantly score inbound leads and alert account executives immediately when enterprise budgets are detected.
- **Real Estate Agents:** Send immediate WhatsApp follow-ups to high-intent inquiries to secure viewings faster.
- **E-commerce Stores:** Nurture high-cart abandonments and send automated discount codes after 24 hours of inactivity.

## 🏗️ Architecture & Features

- **🧠 Automated Lead Scoring:** Evaluates inbound data (e.g., budget and urgency) to categorize leads instantly.
- **🔀 Multi-Channel Routing:** 
  - *Hot Leads* are engaged instantly via a simulated WhatsApp outreach branch.
  - *Warm/Cold Leads* receive an automated Email drip campaign.
- **🤖 Delayed Nurturing:** Uses advanced Wait nodes to pause the workflow for a specified period (e.g., 24 hours), then checks if the customer purchased. If not, it automatically sends a discount code to close the deal.
- **💬 Centralized Notifications:** Merges all branches to send a unified Slack/Email alert to your sales team with the outcome of the initial contact.

## 🚀 How to Use It (Quickstart)

### 1. Prerequisites
- An active [n8n](https://n8n.io/) instance (cloud or self-hosted)
- Credentials for your chosen CRM (e.g., Salesforce) and Messaging platforms (WhatsApp, Slack/Email)

### 2. Installation
1. Clone this repository or download the `workflow.json` file.
2. In your n8n workspace, click **Add Workflow** -> **Import from File**.
3. Select the `workflow.json` file.

### 3. Configuration
1. **Trigger Setup:** Replace the Manual Trigger with a Webhook or Form Trigger node matching your lead source.
2. **CRM Integration:** Add your real credentials to the "Save in Salesforce" node or swap it out for your preferred CRM (HubSpot, Pipedrive).
3. **Wait Node:** The "Wait 1 Day" node is currently configured to 1 minute for testing purposes. Before deploying to production, adjust the parameters to wait `1 Day`.

---

<div align="center">
  <i>Built with ❤️ for the automation and sales community.</i><br>
  Created by <a href="https://github.com/Mosec2525">Mohammad Almashahreh</a>
</div>
