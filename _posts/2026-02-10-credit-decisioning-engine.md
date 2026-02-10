---
layout: post
title: "Credit Decisioning Engine (PD + Pricing + Limit Assignment)"
---

## What this is
This project implements an end-to-end credit decisioning engine using
LendingClub-style consumer loan data. The objective is to demonstrate how
predicted default risk can be translated into practical lending decisions,
rather than focusing solely on model accuracy.

## Why it matters
Demonstrates how a modern lender separates:
- approval
- pricing
- limit assignment  
while balancing growth vs risk-adjusted returns.

### Key components
- **PD modelling** using logistic regression and time-based train/test splits
- **Risk banding** via quantile-based bucketing for stable policy evaluation
- **Approval logic** based on configurable PD thresholds
- **Risk-based pricing** and **approved amount assignment**
- **Portfolio-level evaluation** using observed default outcomes

## Repo
👉 [View the GitHub repo](https://github.com/ancienttemple12/credit-decisioning-engine)
