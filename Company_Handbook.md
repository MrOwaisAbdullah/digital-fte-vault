---
version: platinum-1.0
last_updated: 2026-05-13
---

# Company Handbook — Platinum Tier

## Agent Roles

### Cloud Agent (Oracle VM)
**CAN do autonomously:**
- Triage incoming emails (label, categorize, prioritize)
- Draft email replies (save to /Pending_Approval/, never send directly)
- Draft social media posts (save to /Pending_Approval/, never post directly)
- Create Plan files for complex tasks
- Write status updates to /Updates/
- Query Odoo for financial data (read-only)

**CANNOT do:**
- Send any email
- Post to any social media
- Access WhatsApp
- Make any payment
- Confirm/post Odoo invoices
- Write to Dashboard.md

### Local Agent (Your Machine)
**CAN do autonomously:**
- Execute approved email sends (after human moves to /Approved/)
- Execute approved social posts (after human moves to /Approved/)
- Handle WhatsApp messages
- Update Dashboard.md
- Merge /Updates/ into Dashboard
- Archive completed tasks to /Done/

**CANNOT do without approval:**
- Send emails to new contacts
- Make any payment
- Post to social media
- Confirm Odoo invoices > $100

---

## Approval Thresholds

| Action | Threshold | Auto-approve |
|--------|-----------|--------------|
| Email reply (known contact) | Always | ❌ Never |
| Email reply (new contact) | Always | ❌ Never |
| LinkedIn post | Always | ❌ Never |
| Payment | Always | ❌ Never |
| Odoo invoice confirm | Always | ❌ Never |
| File archiving | Automatic | ✅ Yes |
| Dashboard update | Automatic | ✅ Yes |

---

## Claim-by-Move Rule

When a task appears in /Needs_Action/:
1. First agent to move it to /In_Progress/<agent>/ owns it
2. Other agent must skip any file in /In_Progress/
3. Owner moves to /Done/ when complete
4. Never process a file someone else has claimed

---

## Security Rules

1. Secrets (API keys, passwords, tokens) NEVER go in the Shared Vault
2. WhatsApp sessions stay on Local machine only
3. Banking credentials stay on Local machine only
4. Cloud Agent uses read-only Odoo access where possible
5. All actions are logged in /Logs/ with full audit trail
