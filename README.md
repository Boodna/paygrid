# PayGrid Nexus — Autonomous Agentic Escrow, AI Proof-of-Delivery & AG Grid Command Center on PayPal

Built for the **PayPal AI Hackathon 2026**, **PayGrid Nexus** solves the two biggest blockers in **Agentic Commerce**:
1. **Prompt-Injection Financial Hijacking (OWASP LLM01)**: When an autonomous AI agent reads untrusted vendor invoices or web pages, hidden adversarial instructions can trick the agent into sending unauthorized PayPal payments.
2. **Blind Pre-Payment Without Verification**: Standard agent toolkits fire immediate payments before verifying whether the vendor agent actually delivered working code, valid datasets, or SLA-compliant outputs.

## How PayGrid Nexus Works

1. **Autonomous Multi-Agent Quote Negotiation & PayPal Escrow (`v2/checkout/orders`)**: Buyer agents negotiate B2B task quotes down from the initial ask and lock the agreed amount in a PayPal Order (`intent: CAPTURE`) held in escrow.
2. **AI Proof-of-Delivery & SpendGuard Firewall**: Before any PayPal order is created or captured, PayGrid Nexus scans invoice memos for OWASP LLM01 prompt-injection payloads and verifies cryptographic Proof-of-Delivery (unit test hashes, SLA metrics, schema checksums).
3. **Interactive AG Grid Financial Telemetry Matrix**: Embeds **AG Grid** to give human finance and engineering teams real-time multi-column filtering, sorting, safety-score badges, one-click PayPal Order Capture (`POST /v2/checkout/orders/{id}/capture`), and one-click CSV audit exports.

## Quick Start (Zero Dependencies — Runs in 5 Seconds!)

PayGrid Nexus uses pure Node.js 18+ built-in `fetch` and `http` modules on the backend and **AG Grid** on the frontend—meaning **zero `npm install` wait time**!

```bash
# 1. Start the PayGrid Nexus server & AG Grid Dashboard at http://localhost:3000
npm start

# 2. (Optional) Connect live PayPal Developer Sandbox credentials:
PAYPAL_CLIENT_ID="your_sandbox_client_id" PAYPAL_CLIENT_SECRET="your_sandbox_secret" npm start

# 3. In a second terminal, run the autonomous multi-agent CLI simulation:
npm run demo-agents
```

## License
Released under the **MIT License** (see `LICENSE`).
