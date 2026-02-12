# Nexthink Workflows Library

A collection of production-tested Workflows for Nexthink Infinity — automate remediation, notifications, and IT operations at scale.

> **Part of [Butler DEX Enterprise](https://github.com/ButlerDEXEnterprise)** — At Your Enterprise's Service.

---

## 📋 Available Workflows

| Workflow | Category | Description | Tier |
|---|---|---|---|
| [Reboot Reminder](#reboot-reminder) | Compliance | Notifies users with high uptime and offers a scheduled reboot | 🟢 Free |
| [Disk Space Alert](#disk-space-alert) | Storage | Triggers cleanup suggestions when disk space drops below threshold | 🟢 Free |
| [Software Reclamation](#software-reclamation) | Cost Savings | Identifies and flags unused licensed software for removal | 🔵 Premium |

<!-- Add rows as you publish more workflows -->

---

## 🟢 Free Workflows

### Reboot Reminder

**What it does:** Detects devices that haven't rebooted in X days and sends the user a notification with the option to schedule a reboot at a convenient time.

**Why it matters:** Forced reboots disrupt users. This approach gives them control while still enforcing compliance — leading to better patch coverage and fewer helpdesk complaints.

**Use case:** Pair with the [Long Uptime NQL query](https://github.com/ButlerDEXEnterprise/nexthink-nql-library) for full visibility + automated remediation.

<details>
<summary>📥 Setup Instructions</summary>

1. Import the workflow definition into your Nexthink instance
2. Configure the uptime threshold (default: 7 days)
3. Customize the notification message for your organization
4. Test on a pilot group before broad deployment

</details>

---

### Disk Space Alert

**What it does:** Monitors disk space and triggers a workflow when free space drops below a configurable threshold. Sends the user actionable cleanup suggestions.

**Why it matters:** Low disk space causes app crashes, failed updates, and poor user experience. Proactive alerts prevent tickets before they're created.

**Estimated impact:** Reduces disk-space-related support tickets by catching issues early.

<details>
<summary>📥 Setup Instructions</summary>

1. Import the workflow definition
2. Set your free space threshold (default: 10%)
3. Customize cleanup suggestions for your environment
4. Deploy to target device scope

</details>

---

## 🔵 Premium Workflows

### Software Reclamation

**What it does:** Identifies licensed software that hasn't been used in X days, notifies the user, and automates the reclamation process if no response is received within a grace period.

**Why it matters:** Most enterprises are paying for 20-40% more software licenses than they actually need. This workflow automates the identification, notification, and reclamation cycle — turning unused licenses into real cost savings.

**Estimated savings:** Varies by environment, but typically $50-200 per reclaimed license.

> **This is a premium solution.** The workflow logic and approach are documented here, but the production implementation is available through a consulting engagement. [Contact us](https://github.com/ButlerDEXEnterprise) to discuss your environment.

---

## 📁 Repository Structure

```
nexthink-workflows/
├── README.md
├── LICENSE
├── free/
│   ├── reboot-reminder/
│   │   ├── README.md
│   │   └── workflow-definition.json
│   └── disk-space-alert/
│       ├── README.md
│       └── workflow-definition.json
└── premium/
    └── software-reclamation/
        └── README.md          # Description + contact info only
```

---

## 🚀 Getting Started

### Prerequisites
- Nexthink Infinity with Workflows enabled
- Appropriate permissions to create and manage Workflows
- API access for automated triggering (optional — see [NexthinkAPI PowerShell module](https://github.com/NexthinkGuru/NexthinkAPI))

### Import a Workflow
Each free workflow folder contains everything you need:
1. Review the README in the specific folder
2. Import the workflow definition into your Nexthink instance
3. Configure thresholds and messaging for your environment
4. Test on a small device group first
5. Scale to your full environment

---

## ⚠️ Disclaimer

These workflows are provided as-is. Always test in a non-production environment first. The author is not responsible for any unintended effects. This is not affiliated with or supported by Nexthink S.A.

---

## 📄 License

MIT License — free to use, modify, and contribute.
