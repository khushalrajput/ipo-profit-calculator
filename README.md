# IPO Profit Settlement Calculator

A single-page calculator that computes profit, tax, and settlement between an **Investor (User A)** and an **IPO Applicant (User B)**.

## How It Works

1. User A gives User B a fixed amount (default ₹15,000) to apply for an IPO
2. The actual IPO application amount is usually slightly below the investment
3. If the IPO is allotted and sold at a profit, the profit is calculated on the **actual IPO amount**
4. Tax is deducted from the gross profit
5. Remaining profit is split 50/50 between A and B
6. The calculator shows **how much B must transfer back to A**

## Two Settlement Modes

### Tax-Adjusted Split (Default)
- Tax is deducted from gross profit first
- Net profit (after tax) is split 50/50
- B receives the tax amount as part of settlement (B is the account holder responsible for tax)

### Direct Profit Split (Checkbox)
- Gross profit is split 50/50 directly — no tax deduction before splitting
- A gets investment + 50% of gross profit
- B gets 50% of gross profit and pays tax from their own share

## Key Output

- **B Must Transfer to A**: Original investment + A's profit share
- **B Retains**: B's profit share (+ tax in standard mode)
- Complete money flow visualization
- Quick formula reference
- Copy-to-clipboard summary

## Tech Stack

- HTML + JavaScript + Tailwind CSS (CDN)
- No backend, no database, no build step
- Single `index.html` file — open in any browser

## Inputs

| Field | Default | Description |
|-------|---------|-------------|
| Investment Amount | ₹15,000 | Fixed amount A gives B |
| Actual IPO Amount | ₹14,877 | Amount used for IPO application |
| Profit % | 22% | Profit on actual IPO amount |
| Tax % | 20% | Tax on gross profit |

## Validation

- Investment amount must be positive
- Actual IPO amount cannot exceed investment amount
- Profit % must be non-negative
- Tax % must be between 0% and 100%

## Usage

Open `index.html` in a browser. No installation required.
