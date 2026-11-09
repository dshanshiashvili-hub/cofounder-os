---
name: unit-economics
description: Build and stress-test unit economics (CAC, contribution margin after returns and fees, payback, inference costs). Use for pricing decisions, business-model checks, and before any paid acquisition.
---

# Unit economics

## Model (per customer or per order, whichever fits)
- Price (net of VAT/discounts)
- − COGS (product, fulfilment, shipping both ways)
- − Returns and refunds (rate × cost per return)
- − Payment fees
- − Variable infra / AI inference cost per active user
- = **Contribution margin**
- CAC by channel (fully loaded: ad spend, creator fees, tools, founder hours at a stated rate)
- **CAC payback** = CAC / monthly contribution margin per customer
- LTV only from observed retention; before that, show scenarios, not a number.

## Rules
- Build it in a spreadsheet (xlsx skill or Google Sheets) with inputs separated from formulas.
- Three scenarios: pessimistic / base / optimistic, with the assumption IDs each input depends on.
- Find the **break point**: which single input, moved how far, makes the model fail? Report it.
- Flag any business that only works at a scale it hasn't reached.
