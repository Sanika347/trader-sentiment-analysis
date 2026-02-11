
# Trading Sentiment Analysis

This project analyzes trader performance using Fear & Greed Index.

## Data
- historical_data.csv
- fear_greed_index.csv

# 1. Methodology
Data Sources

Two datasets were used in this analysis:

1.Historical Trader Data (Hyperliquid):
Contains trade-level information such as account ID, execution price, trade size, direction, timestamp, and closed PnL.

2.Bitcoin Fear & Greed Index:
Provides daily market sentiment classified as Fear or Greed.

1]Data Preparation

Loaded both datasets using Pandas.

Converted timestamps into datetime format.

Extracted the daily date from timestamps.

Removed invalid and missing date values.

Merged both datasets on the daily date field.

Cleaned numeric columns such as PnL and trade size.

Removed records with missing critical values.

2]Feature Engineering

**The following key metrics were created:

Daily PnL per account

Win/Loss indicator per trade

Win rate per trader

Average trade size

Trades per day

Long/Short ratio

Total PnL per account

Segmentation

**Traders were grouped into segments:

Frequent vs Infrequent traders (based on median trade count)

Winners vs Losers (based on total PnL)

Performance consistency using average PnL

Analysis Approach

Aggregated metrics by sentiment category.

Compared performance across Fear and Greed days.

Analyzed behavioral changes.

Visualized results using Matplotlib.

Generated summary tables for reproducibility.

# 2. Key Insights
# Insight 1: Performance Differs by Market Sentiment

Average PnL is higher on Greed days compared to Fear days.

Win rate is also higher during Greed periods.

Fear days show more frequent losses and higher volatility.

This indicates that market optimism is associated with better trading outcomes.

# Insight 2: Traders Change Behavior Based on Sentiment

Traders place more trades on Greed days.

Average trade size increases during Greed periods.

On Fear days, traders reduce position sizes and trade less frequently.

This suggests risk-taking behavior increases in positive market sentiment and decreases in negative sentiment.

# Insight 3: Segment-Based Performance Differences

Frequent traders outperform infrequent traders in most conditions.

Winner traders maintain positive PnL even during Fear periods.

Infrequent losers suffer the highest losses during Fear days.

Experienced and active traders adapt better to sentiment changes.

# 3. Strategy Recommendations
# Strategy 1:
Risk Management During Fear Periods

During Fear days:
Reduce position sizes
Limit trading frequency
Avoid high-risk trades

This helps minimize losses during volatile and uncertain market conditions.

# Strategy 2:
Controlled Aggression During Greed Periods

During Greed days:
Frequent and consistent winners may increase trade frequency moderately
Use slightly larger position sizes with strict stop-loss rules
Avoid over-leveraging

This allows traders to benefit from positive sentiment while controlling downside risk.

#Strategy 3: 
Segment-Based Trading Rules

Infrequent traders should avoid active trading during Fear periods.
Frequent winners can be more active in Greed phases.
Losers should focus on capital preservation rather than aggressive trading.
Personalized strategies based on trader profile improve long-term performance.

# 4. Conclusion

This analysis shows that market sentiment significantly influences trader performance and behavior.
Greed periods encourage higher risk-taking and better returns, while Fear periods increase volatility and losses.
Segment-based strategies and adaptive risk management can improve trading outcomes.

By combining sentiment indicators with behavioral metrics, traders and platforms can design smarter and safer trading systems.
