- [ ] 5. Implement the **AWS Step Function** to trigger the Glue Job based on the success status of Lambda function
- [ ] 4. Implement Glue Job Bookmark instead of using 3
- [x] 3. Create a Glue ETL to generate the `t2_multi_factor_data as A` table from `t1_multi_secmaster as B` and `t1_factor_master_definition`
  - [x] read _datetrading_ from both `A` and `B` compare what is the _datetrading_ missing in `B` so we will only load `A` with those _datetrading_ using `push_down_predicate`
- [x] 2. Ignore last column `Unnamed: 49`in secmaster cos it just 90 DAYS average sum
- [x] 1. Date Trading:
  - Col Y: **Consensus Estimate** (consensus: what is majority view) DB (from Broker, so some of stocks not be covered by the broker, so causing NA) -> ANALYSTCOV: also NA () -> how many analysis has covered this stock (#num up vs #num down, mean of EPS, median of EPS, std of EPS) -> Uncertainty measurement (half of community said going up, etc)
    Fundamental Analyst: have the access with company to write the report (projected cashflow, balance sheet -> likely Earning per Share) abt that stock -> Broker can upgrade the rating abt the stock
  - Col AA: Pricing database
    - so it will have all trading date
