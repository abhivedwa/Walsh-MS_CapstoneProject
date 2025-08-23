# Walsh-MS_CapstoneProject

**Dataset name. MS_Capstone_Final_Raw_Dump.xlsx**

**Unit of analysis. Quarterly earnings event for a listed Indian company (one row per company-quarter).**

**Coverage:** 45 NSE/BSE-listed companies across five sectors (IT/Technology, BFSI, FMCG, Pharma, Auto), spanning ~Q2 FY23 (July 2022) through ~Q1 FY26 (July 2025).

**Granularity.** Structured fundamentals reported for the quarter, plus closing prices on the result day (T) and the next three trading days (T+1, T+2, T+3).

Intended use. Supervised classification of 3-day post-earnings price direction using only structured financials and event-day prices (no text/sentiment/technicals), as described in your capstone synopsis. 

**What each column represents: Identifiers & event metadata**

**Company, Ticker** – issuer name and trading symbol used throughout the pipeline.
    AV_Ticker.BSE (helper symbol for price backfill for Aplha Vantage API) 

**Sector, Cap Category** – sector bucket and market-cap tier used for stratified analyses.

**Period** – reporting period label (e.g., Jun 2024 or Q1 FY26).

**Result Date** – official earnings announcement date (event anchor).

**Structured quarterly fundamentals** (as available per company type)

    Sales (a.k.a. revenue for non-financials), Operating Profit, OPM %, Other Income, Interest, Depreciation, Profit before tax (PBT), Tax %, Net Profit, EPS in Rs.

    Revenue, Financing Profit, Financing Margin %, (BFSI-specific – appears where applicable).

Note: Some issuers (esp. banks/NBFCs) report Revenue rather than Sales and provide financing/NPA fields instead of manufacturing-style margins. 

**Event-window prices (closing):**

    _T_date, Closing Price (T) – result-day close (or previous trading day if no trade on result date).

    _T1_date, Closing Price (T+1) – next trading day close.

    _T2_date, Closing Price (T+2) – second trading day close.

    _T3_date, Closing Price (T+3) – third trading day close.
    

**3-Day Avg Price Post Result:** Avg of Closing Price of T+1, T+2, T+3.

**3-Day Return (%):** =ROUND(((3-Day Avg Price Post Result-T)/T)*100,2)

**Movement Label (1,0):** =IF(3-Day Return (%) >= 1, 1, 0)

**Source links:**

    ---> IndianAPI (documentation/landing)

        Quarterly results (to get Result Date):

            https://stock.indianapi.in/historical_stats?stock_name=<TICKER>&stats=quarter_results

        Daily prices (daily-like only):

            https://stock.indianapi.in/historical_data?stock_name=<TICKER>&period=1yr&filter=price

    ---> NSE India (company classification / filings)

    ---> BSE/NSE bhavcopy documentation

    ---> Alpha Vantage (TIME_SERIES_DAILY) API

            https://www.alphavantage.co/query?function=TIME_SERIES_DAILY&symbol=<BSE_TICKER>.BSE&outputsize=full&apikey=<KEY>
    
   

