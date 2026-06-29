# InvestIQ – Teen Investment Manager
## Complete User Guide

---

## Welcome to InvestIQ

InvestIQ is a personal investment tracker designed for teens learning to invest in stocks and bonds. It converts your Excel spreadsheet into a full web app that works in any browser — and can even be installed on your phone like a real app.

**Key facts:**
- All your data is saved **on your device only** — nothing is sent to the cloud.
- Works offline after the first load.
- Installable on iPhone and Android as a home screen app (see [Mobile Setup](#mobile-setup)).
- Built from your original Excel spreadsheet with all 10 modules recreated.

---

## Getting Started

1. Open `index.html` in any modern browser (Chrome, Safari, Edge, Firefox).
2. Go to **⚙️ Settings** and enter your name and starting capital (default: $100,000).
3. Optionally, get a free API key at [alphavantage.co](https://www.alphavantage.co/support/#api-key) for live price updates.
4. Start adding your investments in the **📈 Stocks** or **🏦 Bonds** tabs.

---

## Mobile Setup (Install as an App)

### iPhone / iPad
1. Open `index.html` in **Safari** (must be Safari, not Chrome).
2. Tap the **Share** button (box with arrow pointing up).
3. Scroll down and tap **"Add to Home Screen"**.
4. Name it **InvestIQ** and tap **Add**.
5. The app now appears on your home screen with an icon — just like a real app!

### Android
1. Open `index.html` in **Chrome**.
2. Tap the **three-dot menu** (⋮) in the top right.
3. Tap **"Add to Home Screen"** or **"Install App"**.
4. Tap **Add** to confirm.

---

## Module Guide

### 📊 Dashboard (Performance Summary)
*Corresponds to: "Performance Summary" tab in Excel*

Your at-a-glance portfolio overview. This is the home screen.

**What you see:**
- **Portfolio Value** — Total current value of all your stocks, bonds, and cash.
- **Total P&L** — Your overall profit or loss since you started. Green = winning, Red = losing.
- **Open P&L** — Unrealized gain/loss on positions you still hold (paper profits/losses).
- **Closed P&L** — Realized gain/loss from trades you've already closed.
- **Win Rate** — What % of your closed trades were profitable. 50%+ is great!
- **Cash Available** — How much of your starting capital is undeployed.
- **Portfolio Allocation chart** — How your money is split between Stocks, Bonds, and Cash.
- **Investment Type Mix** — Breakdown by individual stocks, ETFs, mutual funds, bonds, etc.
- **Recent Activity** — Your last 10 transactions.

**Actions:**
- **📸 Log Snapshot** — Quickly saves today's portfolio value to the Growth tracker.

---

### 📈 Stock & Mutual Fund Portfolio
*Corresponds to: "Stock & Mutual Fund Portfolio" + "SMFP Mirror" tabs in Excel*

Track all your open (active) stock, ETF, and mutual fund positions.

**How to add a position:**
1. Click **+ Add Position**.
2. Fill in:
   - **Date** — When you bought it.
   - **Ticker** — The stock symbol (e.g., AAPL for Apple, SPY for S&P 500 ETF).
   - **Company Name** — Optional but helpful.
   - **Position Type** — "Long" means you buy it hoping it goes up. "Short" means you're betting it goes down.
   - **Investment Type** — Individual Stock, ETF, Bond ETF, Traditional Mutual Fund, or Bond Mutual Fund.
   - **Buy Price** — Price per share when you bought.
   - **Shares** — How many shares you own.
   - **Current Price** — Today's price (update manually or use the 🔄 Live Prices button).
   - **Duration** — Long-Term (L) = holding > 1 year, Short-Term (S) = holding < 1 year.
   - **Target Price** — Your goal price to sell.
3. The **Total Invested**, **Value Now**, **P&L**, and **Return %** calculate automatically.

**Columns explained:**
| Column | Meaning |
|--------|---------|
| Buy $ | Price you paid per share |
| Shares | Number of shares owned |
| Invested | Total money you put in (Buy $ × Shares) |
| Current $ | Today's price |
| Value | What it's worth now (Current $ × Shares) |
| P&L $ | Profit or loss in dollars |
| P&L % | Return percentage |
| Duration | L = Long-Term, S = Short-Term |
| Target $ | Your target sell price |

**Closing a position:**
Click the **✓** button on any row to close a trade. Enter the date and price you sold at — the realized P&L is recorded automatically and moves to Trade History.

**Live Price Updates:**
Click **🔄 Live Prices** to fetch current prices from Alpha Vantage (free API key required in Settings). The free tier allows 25 price lookups per day.

---

### 📉 Stock & Mutual Fund History
*Corresponds to: "Stock & Mutual Fund History" + "SMFH Mirror" tabs in Excel*

A complete record of all your closed (completed) trades.

**What you see:**
- Every trade you've closed, newest first.
- Columns for both the open date and close date.
- Buy price vs. close price for easy comparison.
- Realized P&L — this is real money made or lost.
- Win Rate at the top (how often you close trades profitably).

**Tip:** Review your history regularly to learn from your winners and mistakes. Did you sell too early? Hold too long? The history helps you improve.

---

### 🏦 Bond Portfolio
*Corresponds to: "Bond Portfolio" tab in Excel*

Track your active bond investments. Bonds are loans you make to governments or companies — they pay you regular interest and return your money at maturity.

**Bond basics:**
- **Face Value** — The amount the bond pays back at maturity (e.g., $1,000).
- **Coupon Rate** — Annual interest rate (e.g., 4.5% means $45/year per $1,000 bond).
- **Purchase Price** — What you paid (can be more or less than face value).
- **Maturity Date** — When the bond expires and pays back the face value.

**Bond Types:**
- 🏛️ **Treasury** — Issued by the U.S. government. Safest option.
- 🏢 **Corporate** — Issued by companies. Higher interest, more risk.
- 🏘️ **Municipal** — Issued by cities/states. Often tax-advantaged.

**Auto-calculated fields:**
| Field | Formula |
|-------|---------|
| Total Invested | Purchase Price × Quantity |
| Total Face Value | Face Value × Quantity |
| Annual Interest | Face Value × Coupon Rate × Quantity |
| Total Interest | Annual Interest × Length (Years) |
| Maturity Value | Total Face Value + Total Interest |
| Maturity Date | Start Date + Length in Years |

**Payout Frequencies:** Annual, Semi-Annual (every 6 months), Quarterly (every 3 months), Monthly.

---

### 📋 Bond History
*Corresponds to: "Bond History" tab in Excel*

Your closed bond positions — bonds that have matured (reached their end date) or that you sold early.

- **Matured** = Bond reached its end date, you received face value + all interest.
- **Sold Early** = You sold before maturity (may receive more or less than face value).

---

### 🥧 Diversification Tracker
*Corresponds to: "Diversification Tracker" + "HS Mirror" + "IT Mirror" tabs in Excel*

See how balanced your portfolio is across different investment types.

**Holding Strategy Breakdown:**
| Category | What It Includes |
|----------|-----------------|
| Long-Term | Long positions with Duration = L (>1 year) |
| Short-Term | Long positions with Duration = S (<1 year) |
| Short Positions | Any Short (betting against) positions |
| Cash | Uninvested capital remaining |

**Investment Type Breakdown:**
| Type | Examples |
|------|---------|
| Stock | Individual company shares |
| ETF | Exchange-Traded Funds (e.g., SPY, QQQ) |
| Bond ETF | ETFs that hold bonds |
| Mutual Fund | Traditional or Bond mutual funds |
| Bond | Treasury, Corporate, Municipal bonds |
| Cash | Uninvested funds |

**Diversification Tips:** The app analyzes your portfolio and provides personalized suggestions — like warning if you're too concentrated in one asset type or have too much cash sitting idle.

**Rule of thumb for teen investors:**
- 60–70% Stocks/ETFs (for growth)
- 20–30% Bonds (for stability)
- 5–15% Cash (for opportunities)

---

### 👁️ Watchlist
*Corresponds to: "Watchlist" tab in Excel*

Track stocks and ETFs you're researching but haven't bought yet.

**Fields:**
- **Ticker** — Stock symbol.
- **★ Star** — Star your highest-priority watches.
- **Current Price / Daily %** — Update manually to track movement.
- **Target Buy** — Price at which you'd consider buying.
- **Target Sell** — Your exit target once you own it.
- **Priority** — 🔴 High, 🟡 Medium, 🟢 Low.
- **Action** — Watch, Buy Soon, Research, or Avoid.
- **Notes** — Your investment thesis: *Why* are you watching this?

**📈 Move to Portfolio:** Click the 📈 button to instantly move a watchlist item to your stock portfolio pre-filled with its data.

**Best practice:** Write your investment thesis in Notes before buying. If you can't explain why you're buying it in 2 sentences, do more research first.

---

### 📰 Live News
*Corresponds to: "Live News" tab in Excel*

Quick links to news and analysis for every ticker in your portfolio and watchlist.

For each ticker, you get direct links to:
- **Yahoo Finance** — Breaking news and earnings
- **Google Finance** — Quick price charts
- **Stock Analysis** — Detailed fundamentals
- **Finviz** — Visual charts and technical analysis
- **Seeking Alpha** — In-depth investor articles

**Note:** The original Excel used Google Finance and Finnhub APIs which require paid keys. This app links directly to free news sources that don't require any API keys.

---

### 🎯 S&P 500 Benchmark
*Corresponds to: "S&P 500" tab in Excel*

Compare your portfolio performance against the S&P 500 Index — the benchmark all professional investors are measured against.

**Setup:**
1. Click **✏️ Update Benchmark**.
2. Enter the S&P 500 level when you started investing (check historical data at finance.yahoo.com/quote/^GSPC).
3. Enter today's current S&P 500 level.
4. The app calculates whether you're beating or trailing the market.

**What it means:**
- **You vs S&P 500** — If positive, you're beating the market (better than most pros!).
- If negative, the index fund did better than your picks.

**Key insight:** Studies show over 90% of active stock pickers fail to beat the S&P 500 over 10+ years. If you're beating it consistently, you have real skill!

---

### 📅 Portfolio Growth
*Corresponds to: "Portfolio Growth" tab in Excel*

Track your portfolio value over time and visualize growth vs. the S&P 500.

**How it works:**
1. Click **+ Log Entry** (or use **📸 Log Snapshot** from the Dashboard).
2. Enter the date, your current portfolio value, and the current S&P 500 level.
3. Do this weekly or monthly to build a growth chart.

**The chart shows:**
- 📈 **Your Portfolio** (green line) — actual dollar value over time.
- 📊 **S&P 500 Indexed** (blue dashed) — what the same starting capital would be worth in an index fund.

**Table columns:**
- **Portfolio P&L** — How much you've made/lost since start.
- **S&P 500 Return** — What % the index returned since your first snapshot.
- **You vs S&P** — Your outperformance (positive = beating the market).

---

### ⚙️ Settings

Configure your account and manage your data.

**Settings:**
- **Your Name** — Personalizes the app.
- **Starting Capital** — Your initial investment amount (default: $100,000).
- **Alpha Vantage API Key** — For live price fetching. Free key at [alphavantage.co](https://www.alphavantage.co/support/#api-key).

**Data Management:**
- **Export JSON** — Download a backup of all your data. Do this regularly!
- **Import JSON** — Restore from a backup file.
- **Reset All Data** — Clear everything and start fresh (cannot be undone).

---

## Tips for Teen Investors

### The Basics
1. **Start with index funds (ETFs)** like SPY or QQQ before picking individual stocks.
2. **Never invest money you need** in the next 1–2 years. The market can drop temporarily.
3. **Diversify** — don't put all your money in one stock.
4. **Think long-term** — historically, the S&P 500 returns ~10% per year on average over long periods.

### Using InvestIQ Well
- Log a portfolio snapshot **weekly** to build a meaningful growth chart.
- Update current prices **at least monthly** to see accurate P&L.
- Use the **Watchlist** to research before buying — impulsive buys often lose money.
- Review your **Trade History** quarterly to learn from both wins and losses.
- Check the **Diversification tracker** monthly to rebalance if one asset class gets too large.

### Understanding P&L
- **Unrealized P&L (Open)** = Paper profit — you haven't actually made this money yet.
- **Realized P&L (Closed)** = Real profit/loss — money you've actually gained or lost.
- A stock can look profitable on paper, then drop before you sell. Lock in profits by setting target prices.

---

## Frequently Asked Questions

**Q: Is my data safe?**
A: Yes. Everything is stored in your browser's localStorage — on your device only. Nothing leaves your device.

**Q: What if I change browsers or computers?**
A: Use **Export JSON** to save a backup, then **Import JSON** on your new browser/device.

**Q: How do I get live prices?**
A: Get a free API key at alphavantage.co (takes 1 minute), paste it in Settings, then click 🔄 Live Prices. Free tier allows 25 updates/day.

**Q: Why can't I see news in the News tab?**
A: The News tab provides links to external news sites for your tickers. Click any link to open the news in your browser. Add tickers to your Stock Portfolio or Watchlist to populate the list.

**Q: What's the difference between Long-Term and Short-Term duration?**
A: Long-Term (L) = you plan to hold for more than 1 year. Short-Term (S) = you plan to sell within 1 year. This affects your tax rate on profits in real life — long-term capital gains are taxed at a lower rate.

**Q: What is a "short position"?**
A: Shorting means you're betting a stock will go DOWN. This is very risky and generally not recommended for beginners. Most teen investors should only use Long positions.

---

## Keyboard Shortcuts

| Action | Shortcut |
|--------|---------|
| Close any modal | Press `Escape` or click outside it |
| Navigate tabs | Click the tab buttons in the navbar |
| On mobile | Swipe or tap the bottom navigation bar |

---

## Data Backup Reminder

> **Back up your data regularly!** Go to ⚙️ Settings → Export JSON and save the file somewhere safe (Google Drive, iCloud, email to yourself). If you clear your browser data, your investments data will be deleted.

---

*InvestIQ — Built for teens, by teens in mind. Happy investing! 📈*
