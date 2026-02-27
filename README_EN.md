# Qieman Investment Advisory MCP Server

Qieman Investment Advisory MCP Server is an intelligent investment advisory service based on the Model Context Protocol (MCP), providing AI assistants with professional fund analysis, asset allocation, and portfolio diagnostics capabilities. Make investment decisions smarter and more efficient through natural language interaction.

## Core Capabilities

### 📊 Personal & Household Finance Analysis

- **Asset-Liability Analysis**: Intelligent calculation of asset-liability ratios, net worth, and core financial metrics
- **Cash Flow Analysis**: Generate cash flow health reports based on household income/expenses and asset allocation
- **Family Member Analysis**: Statistics on family size and life cycle stages with customized recommendations
- **Financial Indicator Diagnostics**: Assess the rationality of key financial indicators and identify potential risks
- **Income-Expense Structure Analysis**: Visualize annual income/expense distribution and optimize financial planning

### 💼 Fund & Portfolio Analysis

- **Fund Risk Assessment**: Multi-dimensional risk scoring and indicator analysis (volatility, max drawdown, Sharpe ratio, etc.)
- **Portfolio Risk Diagnostics**: Overall portfolio risk assessment and optimization recommendations
- **Holdings Diagnostics**: In-depth analysis of fund allocation rationality, correlation, and historical backtesting performance
- **Asset Allocation Analysis**: Fund portfolio asset class penetration to identify hidden risks
- **Correlation Analysis**: Discover correlations between funds to avoid over-concentration
- **Backtesting Simulation**: Historical data backtesting and Monte Carlo simulation to predict future return ranges

### 🔍 Fund Information Query

- **Fund Details**: Batch retrieval of comprehensive fund information including NAV, performance, holdings, and fees
- **Performance Diagnostics**: Fund risk level, valuation level, and performance attribution analysis
- **Smart Search**: Support fuzzy matching of fund names and multi-dimensional filtering and sorting
- **Popular Funds**: Real-time tracking of popular market funds and investment trends
- **Announcement Query**: Timely access to fund announcements, trading rules, and limit information

### 📈 Professional Investment Analysis

- **Industry Allocation Analysis**: Fund industry preferences, concentration, and revenue contribution analysis
- **Bond Indicators**: Professional bond fund indicators including duration, leverage, and credit ratings
- **Equity Indicators**: Equity position, turnover rate, market timing ability, and Brinson attribution analysis
- **QDII Analysis**: Overseas fund regional allocation and risk assessment
- **Strategy Research**: Fund strategy details, risk information, and asset penetration

### 🛠️ Auxiliary Tools

- **Data Visualization**: ECharts chart rendering for intuitive display of analysis results
- **Report Generation**: HTML to PDF conversion for professional investment reports
- **Real-time News**: Financial news, hot topics, and fund manager viewpoint search
- **AI Interpretation**: Real-time AI news interpretation and investment advisory content recommendations

## Use Cases

### Individual Investors

- Quickly diagnose risk and return characteristics of existing fund portfolios
- Obtain professional asset allocation recommendations and optimization solutions
- Track market hotspots and latest fund manager viewpoints

### Investment Advisors

- Provide clients with professional financial planning and asset allocation services
- Batch analyze fund products and quickly generate investment reports
- Monitor portfolio risks in real-time and adjust investment strategies promptly

### Financial Researchers

- In-depth analysis of fund performance attribution and risk sources
- Research industry allocation trends and market rotation patterns
- Backtest investment strategies and validate investment logic

## Tool List

## Personal & Household Finance Analysis (5)

* AnalyzeAssetLiability - Analyze household assets and liabilities.
* AnalyzeCashFlow - Analyze cash inflows, outflows, and net cash position.
* AnalyzeFamilyMembers - Analyze family-member profile and financial roles.
* AnalyzeFinancialIndicators - Analyze key financial health indicators.
* AnalyzeIncomeExpense - Analyze income and expense structure.

## Fund & Portfolio Analysis (8)

* AnalyzeFundRisk - Assess fund-level risk characteristics.
* AnalyzePortfolioRisk - Assess risk at portfolio level.
* DiagnoseFundPortfolio - Diagnose fund holdings composition and structure.
* GetAssetAllocation - Analyze asset allocation breakdown.
* GetFundAssetClassAnalysis - Perform asset-class look-through analysis.
* GetFundsBackTest - Run portfolio/fund backtesting.
* GetFundsCorrelation - Analyze return correlation among funds.
* MonteCarloSimulate - Run Monte Carlo simulation scenarios.

## Fund Information Query (7)

* BatchGetFundNavHistory - Batch query historical NAV time series.
* BatchGetFundsDetail - Batch query core fund details.
* GetBatchFundPerformance - Batch query fund performance metrics.
* GetFundDiagnosis - Retrieve overall fund diagnosis.
* SearchFunds - Search funds by keyword/criteria.
* GetPopularFund - Retrieve popular/trending funds.
* GuessFundCode - Fuzzy-match fund code from input text.

## Holdings Features & Capability Metrics (7)

* fund-sector-preference - Retrieve sector preference profile.
* fund-equity-position - Retrieve equity exposure preference.
* fund-recovery-ability - Evaluate drawdown recovery capability.
* getFundTurnoverRate - Retrieve turnover rate (rebalancing frequency).
* getFundIndustryPreference - Retrieve industry preference profile.
* getFundIndustryAllocation - Retrieve industry allocation weights.
* getFundIndustryConcentration - Retrieve industry concentration level.

## Holdings / Attribution / Risk Deep-Dive (14)

* getQdFundAreaAllocation - Retrieve QDII geographic allocation.
* getBondFundCreditRatingLevel - Retrieve bond credit-rating distribution.
* getBondAllocationByFundCode - Retrieve bond-type allocation mix.
* getStockAllocationAndMetricsByFundCode - Retrieve equity holdings and valuation/quality metrics.
* getFundIndustryReturns - Retrieve industry-level return contribution.
* getFundBrinsonIndicator - Retrieve Brinson attribution indicators.
* getMarketTimingIndicator - Retrieve market-timing indicators.
* getFundCampisiIndicator - Retrieve Campisi attribution indicators.
* getBondIndicator - Retrieve bond risk indicators (e.g., leverage, duration, concentration).
* getFundDiveCount - Retrieve abnormal-move/event count for bond funds.
* filterBondFundByCreditRating - Filter bond funds by credit-rating criteria.
* filterBondFundByBondType - Filter bond funds by bond-type style.
* filterStockFundByStockTurnover - Filter funds by stock turnover characteristics.
* getBondFundWithAlertRecord - Retrieve bond funds with alert records.

## Basic Info & Trading Rules (6)

* getFundBenchmarkInfo - Retrieve benchmark definition and metadata.
* BatchGetFundTradeRules - Batch query fund trading rules.
* BatchGetFundTradeLimit - Batch query trading limits and constraints.
* BatchGetFundsSplitHistory - Batch query fund split history.
* BatchGetFundsDividendRecord - Batch query dividend distribution records.
* BatchGetFundsHolding - Batch query fund holdings data.

## Strategy & Advisory (9)

* GetStrategyDetails - Retrieve strategy details.
* GetStrategyBenchmark - Retrieve strategy benchmark.
* GetStrategyAssetClassAnalysis - Analyze strategy asset-class distribution.
* BatchGetStrategiesComposition - Batch query strategy holdings composition.
* BatchGetPoTradeComposition - Retrieve strategy trade composition.
* StrategySearchByKeyword - Search strategies by keyword.
* BatchGetStrategyRiskInfo - Batch query strategy risk profiles.
* GetStrategyRiskInfo - Retrieve strategy risk profile.
* GetFundRelatedStrategies - Retrieve advisory strategies related to target funds.

## News & Announcements (7)

* SearchFinancialNews - Search financial news.
* SearchManagerViewpoint - Search fund manager viewpoints.
* searchRealtimeAiAnalysis - Retrieve real-time AI analysis on market/news.
* SearchHotTopic - Retrieve hot financial topics.
* searchInvestAdvisorContent - Search investment-advisory content.
* GetFundAnnouncements - Retrieve fund announcement list.
* GetAnnouncementContent - Retrieve full announcement content.

## Investment Planning & Portfolio (4)

* GetAssetAllocationPlan - Generate/retrieve asset-allocation plan.
* GetCompositeModel - Generate/retrieve composite investment model.
* AnalyzeInvestmentPerformance - Evaluate investment-plan performance.
* GetPortfolioNavHistory - Retrieve portfolio NAV history.

## Market & Utility Tools (5)

* GetLatestQuotations - Retrieve latest market quotes/market thermometer.
* RenderEchart - Render ECharts configuration/output.
* RenderHtmlToPdf - Convert HTML report to PDF.
* GetCurrentTime - Retrieve current system time.
* GetTxnDayRange - Query trading-day range.

## Quick Start

### Access Method: MCP-SSE (Cloud Hosted)

Qieman Investment Advisory MCP Server uses a **cloud-hosted model**. No local server deployment is required; you only need to configure the SSE endpoint in your client. Some clients (such as Claude Desktop) require Node.js/npm to run a bridge command.

### Step 1: Get API Key

1. Visit [Qieman MCP Service Page](https://qieman.com/mcp) to register
2. Apply for and obtain MCP API Key in your personal center
3. Save your API Key (needed for configuration)

> 💡 **Tip**: For detailed configuration guide and API Key management, visit [https://qieman.com/mcp](https://qieman.com/mcp)

### Step 2: Configure in Claude Desktop

Add to your Claude Desktop configuration file:

```json
{
  "mcpServers": {
    "qieman": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://stargate.yingmi.com/mcp/sse?apiKey=your-api-key-here"
      ]
    }
  }
}
```

**Configuration Notes**:

- `mcp-remote`: Bridges a remote SSE MCP server to local stdio (recognized by Claude Desktop)
- `https://stargate.yingmi.com/mcp/sse?apiKey=your-api-key-here`: Qieman MCP SSE endpoint (replace `your-api-key-here` with your real API Key)

### Step 3: Use in Other MCP Clients

#### Cursor IDE

**Configuration Steps**:

1. Open Cursor, click **Settings**
2. Click **MCP**
3. Click **Add MCP Server**
4. Enter the following configuration and save:

```json
{
  "mcpServers": {
    "Qieman": {
      "url": "https://stargate.yingmi.com/mcp/sse?apiKey=your-api-key-here"
    }
  }
}
```

**Configuration Notes**:

- Replace `your-api-key-here` with your actual API Key
- Cursor download: [https://www.cursor.com/cn](https://www.cursor.com/cn)

#### Cherry Studio

**Configuration Steps**:

1. Open Cherry Studio
2. Type selection: **sse**
3. Enter MCP Server address:

```
https://stargate.yingmi.com/mcp/sse?apiKey=your-api-key-here
```

**Configuration Notes**:

- Replace `your-api-key-here` with your actual API Key
- Connection type must be: **sse**
- Cherry Studio download: [https://cherry-ai.com/](https://cherry-ai.com/)

**Recommended Configuration** (Optional):

- Recommended model: Volcano Engine Deepseek-v3 model
- Model name: `deepseek-v3-250324`

#### Windsurf / Trae / Other IDEs

Add to corresponding configuration file:

URL parameter method directly:

```json
{
  "mcpServers": {
    "qieman": {
      "url": "https://stargate.yingmi.com/mcp/sse?apiKey=your-api-key-here"
    }
  }
}
```

> ⚠️ Compatibility note: MCP transport support varies by client. Please verify that your client supports remote SSE MCP.

### Usage Examples

**Scenario 1: Diagnose Fund Portfolio**

```
I hold the following funds: E Fund Blue Chip Select (005827), Xingquan Heren (163406), China Europe Pioneer (001938). Please analyze the portfolio's risk and correlation.
```

**Scenario 2: Asset Allocation Recommendation**

```
I have 1 million yuan in capital with moderate risk tolerance and expect an annualized return of around 8%. Please design an asset allocation plan for me.
```

**Scenario 3: Performance Attribution Analysis**

```
Using the Campisi model, break down the total return of Huaxia Bond Fund Class A (fund code: 001001) from June 30 to September 30, 2025. What are the contribution ratios of interest rate changes, credit spread movements, coupon income, and other factors?
```

## Technical Features

- **Cloud Hosted**: No local server deployment required; connect by configuring the SSE URL in your client
- **Professional & Reliable**: Based on Qieman's years of accumulated financial data and analytical models
- **Real-time Updates**: Support real-time retrieval of latest fund NAV, announcements, and market news
- **Intelligent Analysis**: Combined with AI capabilities for natural language interactive investment analysis
- **Visualization**: Built-in chart rendering and report generation for clear results
- **Standard Protocol**: Based on MCP protocol, compatible with Claude Desktop, Cursor, Trae and other mainstream AI tools
- **Secure & Controlled**: API Key authentication, encrypted data transmission for information security

## Disclaimer

All information, analysis, and recommendations provided by this service are for reference only and do not constitute any investment advice or guarantee. Investment involves risks, and decisions should be made with caution. The developers and service providers are not responsible for any investment losses resulting from the use of this service. Please make investment decisions based on your own circumstances with a full understanding of the risks.

## License

MIT License

## Contact

- GitHub: [@Chris1Wang3](https://github.com/Chris1Wang3)
- Issue Tracker: wangjaye@yingmi.cn
- Official Website: [https://qieman.com/mcp](https://qieman.com/mcp)

---

**Powered by Qieman Investment Advisory with Professional Financial Data Support**
