# Qieman Investment Advisory MCP Server

Qieman Investment Advisory MCP Server is an intelligent investment advisory service based on the Model Context Protocol (MCP), providing AI assistants with professional fund analysis, asset allocation, and portfolio diagnostics capabilities. Make investment decisions smarter and more efficient through natural language interaction.

## Core Capabilities

### 📊 Asset & Family Financial Analysis
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

## Main Tool List

### Asset & Family Financial Analysis
- `AnalyzeAssetLiability` - Asset-liability analysis
- `AnalyzeCashFlow` - Cash flow analysis
- `AnalyzeFamilyMembers` - Family member analysis
- `AnalyzeFinancialIndicators` - Financial indicator analysis
- `AnalyzeIncomeExpense` - Income-expense analysis
- `AnalyzeInvestmentPerformance` - Investment performance evaluation

### Fund & Portfolio Analysis
- `AnalyzeFundRisk` - Fund risk analysis
- `AnalyzePortfolioRisk` - Portfolio risk assessment
- `DiagnoseFundPortfolio` - Fund holdings diagnostics
- `GetAssetAllocation` - Asset allocation analysis
- `GetFundAssetClassAnalysis` - Asset class penetration
- `GetFundsBackTest` - Portfolio backtesting
- `GetFundsCorrelation` - Correlation analysis
- `MonteCarloSimulate` - Monte Carlo simulation

### Fund Information Query
- `BatchGetFundNavHistory` - Batch NAV history retrieval
- `BatchGetFundsDetail` - Batch fund details retrieval
- `GetBatchFundPerformance` - Batch performance metrics
- `GetFundDiagnosis` - Fund diagnostics
- `SearchFunds` - Fund search
- `GetPopularFund` - Popular funds

### Professional Analysis Tools
- `getFundIndustryAllocation` - Industry allocation analysis
- `getBondIndicator` - Bond indicators
- `getFundBrinsonIndicator` - Brinson attribution
- `getMarketTimingIndicator` - Market timing indicators
- `GetStrategyDetails` - Strategy details

### Auxiliary Tools
- `RenderEchart` - Chart rendering
- `RenderHtmlToPdf` - Report generation
- `SearchFinancialNews` - News search
- `GetCurrentTime` - Time utility

For the complete tool list, please refer to the repository documentation.

## Quick Start

### Access Method: MCP-SSE (Cloud Hosted)

Qieman Investment Advisory MCP Server uses a **cloud-hosted model**. No local installation or code execution required - simply connect via SSE URL.

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
      "args": ["-y", "@modelcontextprotocol/server-sse"],
      "env": {
        "SSE_URL": "https://stargate.yingmi.com/mcp/sse",
        "QIEMAN_API_KEY": "your-api-key-here"
      }
    }
  }
}
```

**Configuration Notes**:
- Replace `your-api-key-here` with your actual API Key
- `SSE_URL`: Qieman MCP service address (fixed value)

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

#### Windsurf / Cline / Other IDEs

Add to corresponding configuration file:

```json
{
  "mcpServers": {
    "qieman": {
      "url": "https://stargate.yingmi.com/mcp/sse",
      "headers": {
        "Authorization": "Bearer your-api-key-here"
      }
    }
  }
}
```

Or use URL parameter method directly:

```json
{
  "mcpServers": {
    "qieman": {
      "url": "https://stargate.yingmi.com/mcp/sse?apiKey=your-api-key-here"
    }
  }
}
```

### Usage Examples

**Scenario 1: Diagnose Fund Portfolio**
```
I hold the following funds: E Fund Blue Chip Select (005827), Xingquan Heren (163406), China Europe Pioneer (001938). Please analyze the portfolio's risk and correlation.
```

**Scenario 2: Asset Allocation Recommendation**
```
I have 1 million yuan in capital with moderate risk tolerance and expect an annualized return of around 8%. Please design an asset allocation plan for me.
```

**Scenario 3: Fund Screening**
```
Please help me screen equity funds with annualized returns exceeding 15% and maximum drawdown less than 20% over the past 3 years.
```

## Technical Features

- **Cloud Hosted**: No local installation required, connect via SSE URL instantly
- **Professional & Reliable**: Based on Qieman's years of accumulated financial data and analytical models
- **Real-time Updates**: Support real-time retrieval of latest fund NAV, announcements, and market news
- **Intelligent Analysis**: Combined with AI capabilities for natural language interactive investment analysis
- **Visualization**: Built-in chart rendering and report generation for clear results
- **Standard Protocol**: Based on MCP protocol, compatible with Claude Desktop, Cursor, Cline and other mainstream AI tools
- **Secure & Controlled**: API Key authentication, encrypted data transmission for information security

## Disclaimer

All information, analysis, and recommendations provided by this service are for reference only and do not constitute any investment advice or guarantee. Investment involves risks, and decisions should be made with caution. The developers and service providers are not responsible for any investment losses resulting from the use of this service. Please make investment decisions based on your own circumstances with a full understanding of the risks.

## License

MIT License

## Contact

- GitHub: [@Chris1Wang3](https://github.com/Chris1Wang3)
- Issue Tracker: [Issues](https://github.com/Chris1Wang3/Qieman-MCP/issues)
- Official Website: [https://qieman.com/mcp](https://qieman.com/mcp)

---

**Powered by Qieman Investment Advisory with Professional Financial Data Support**
