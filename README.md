# Sanctum — Agentic Home Loan Approval (POV Demo)

Point-of-view demo for the **Business Analyst – Data & AI Presales** assignment: lakehouse + one orchestrator AI agent + human credit officer for Indian **home loans**.

## Live demo

**https://sanctum-loan-demo-233971633808.asia-south1.run.app**

(also: https://sanctum-loan-demo-jhstkv5tiq-el.a.run.app)

Hosted on Cloud Run (`asia-south1`), `min-instances=0` → idle cost ≈ ₹0.

## What's included

| Deliverable | Where |
|-------------|--------|
| D1 Demo UI | `web/index.html` → Live demo |
| D2 Approach story | Approach page |
| D3 Architecture | Architecture page |
| D4 About / FAQ / Contact | Supporting pages |
| D5 Research note | `web/docs/research-note.html` (Print → PDF) |
| D6 AI usage log | `web/docs/ai-usage-log.html` (Print → PDF) |

Synthetic data only. Bureau / CERSAI responses are mocks. The agent recommends; it does not sanction.

## Local preview

Open `web/index.html` in a browser, or:

```bash
cd web
npx --yes serve -l 3000
```

## Deploy (Google Cloud Run, near-zero cost)

Uses project `veritas-claims-512706`, scale-to-zero (`min-instances=0`), 128Mi memory.

```bash
gcloud config set project veritas-claims-512706
gcloud run deploy sanctum-loan-demo `
  --source "D:\Niveus\Loan approval\web" `
  --region asia-south1 `
  --allow-unauthenticated `
  --min-instances 0 `
  --max-instances 2 `
  --memory 128Mi `
  --cpu 1 `
  --port 8080
```

Idle cost ≈ ₹0 (scales to zero). Free-tier request/CPU allowances cover light demo traffic.

## Submission checklist

1. Hosted demo URL (Cloud Run)
2. D5 + D6 as PDF (open each HTML → Print → Save as PDF) or links from the Docs page
3. Screen recording ≤ 5 minutes
4. Email subject: `Data & AI Presales Assignment – [Your Name]`
