---
layout: post
title: "Credit Decisioning Engine (PD + Pricing + Limit Assignment)"
---

## Business question
**How should a lender translate predicted default risk into approval, pricing, and limit decisions to maximise risk-adjusted returns?**

This project builds an end-to-end credit decisioning engine using LendingClub-style consumer loan data. The focus is on turning a PD model into **practical underwriting decisions** (not just model accuracy).

## What I built
A modern decisioning flow that separates:
- **approval** (accept / decline)
- **pricing** (APR tiers by risk)
- **limit assignment** (approved amount / exposure)

### Key components
- **PD modelling** using logistic regression with time-based train/test splits (no leakage)
- **Risk banding** via quantile bucketing for stable policy evaluation
- **Approval logic** based on configurable PD cutoffs
- **Risk-based pricing** + **approved amount assignment**
- **Portfolio-level evaluation** using observed default outcomes

---

## Results (portfolio view)

### Chart: default rate by predicted risk band
This shows that the PD model meaningfully orders risk and provides a stable foundation for policy rules (approval cutoffs, APR tiers, and limits).

![Default rate by predicted risk band](/assets/img/credit-engine-default-rate-by-band.png)

### Insights
- Default rates increase monotonically across PD bands, supporting **risk-segmented policies**
- Pricing and limits can be set per band to balance **growth vs loss volatility**
- Portfolio evaluation highlights trade-offs better than model metrics alone

---

## Links
- **Case study:** this page  
- **Repo:** 👉 [View the GitHub repo](https://github.com/ancienttemple12/credit-decisioning-engine)

