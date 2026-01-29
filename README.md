# 且慢投顾 MCP Server

且慢投顾 MCP Server 是一个基于模型上下文协议（MCP）的智能投资顾问服务，为 AI 助手提供专业的基金分析、资产配置、投资组合诊断等金融服务能力。通过自然语言交互，让投资决策更智能、更高效。

## 核心能力

### 📊 资产与家庭财务分析
- **资产负债分析**：智能计算资产负债比率、净资产等核心财务指标
- **现金流分析**：基于家庭收支与资产配置生成现金流健康度报告
- **家庭成员分析**：统计家庭人数与生命周期阶段，提供定制化建议
- **财务指标诊断**：评估关键财务指标的合理性，识别潜在风险
- **收支结构分析**：可视化年度收支分布与占比，优化财务规划

### 💼 基金与组合分析
- **基金风险评估**：多维度风险评分与指标分析（波动率、最大回撤、夏普比率等）
- **组合风险诊断**：基金组合整体风险评估与优化建议
- **持仓诊断**：深度分析基金配置合理性、相关性与历史回测表现
- **资产配置分析**：基金组合资产大类穿透，识别隐藏风险
- **相关性分析**：发现基金间的相关性，避免过度集中
- **回测模拟**：历史数据回测与蒙特卡洛模拟，预测未来收益区间

### 🔍 基金信息查询
- **基金详情**：批量获取基金净值、业绩、持仓、费率等全面信息
- **业绩诊断**：基金风险等级、估值水平、业绩归因分析
- **智能搜索**：支持基金名称模糊匹配、多维度筛选排序
- **热门基金**：实时追踪市场热门基金与投资趋势
- **公告查询**：及时获取基金公告、交易规则、限额信息

### 📈 专业投资分析
- **行业配置分析**：基金行业偏好、集中度与收益贡献分析
- **债券指标**：久期、杠杆、信用评级等债券基金专业指标
- **股票指标**：权益仓位、换手率、择时能力、Brinson归因分析
- **QDII分析**：海外基金地区配置与风险评估
- **策略研究**：基金策略详情、风险信息与资产穿透

### 🛠️ 辅助工具
- **数据可视化**：ECharts 图表渲染，直观展示分析结果
- **报告生成**：HTML 转 PDF，一键生成专业投资报告
- **实时资讯**：财经新闻、热点话题、基金经理观点搜索
- **AI 解读**：实时 AI 资讯解读与投顾内容推荐

## 适用场景

### 个人投资者
- 快速诊断现有基金组合的风险与收益特征
- 获取专业的资产配置建议与优化方案
- 追踪市场热点与基金经理最新观点

### 投资顾问
- 为客户提供专业的财务规划与资产配置服务
- 批量分析基金产品，快速生成投资报告
- 实时监控组合风险，及时调整投资策略

### 金融研究员
- 深度分析基金业绩归因与风险来源
- 研究行业配置趋势与市场轮动规律
- 回测投资策略，验证投资逻辑

## 主要工具清单

### 资产与家庭财务分析
- `AnalyzeAssetLiability` - 资产负债分析
- `AnalyzeCashFlow` - 现金流分析
- `AnalyzeFamilyMembers` - 家庭成员分析
- `AnalyzeFinancialIndicators` - 财务指标分析
- `AnalyzeIncomeExpense` - 收入支出分析
- `AnalyzeInvestmentPerformance` - 投资方案表现评估

### 基金与组合分析
- `AnalyzeFundRisk` - 基金风险分析
- `AnalyzePortfolioRisk` - 组合风险评估
- `DiagnoseFundPortfolio` - 基金持仓诊断
- `GetAssetAllocation` - 资产配置分析
- `GetFundAssetClassAnalysis` - 资产大类穿透
- `GetFundsBackTest` - 组合回测
- `GetFundsCorrelation` - 相关性分析
- `MonteCarloSimulate` - 蒙特卡洛模拟

### 基金信息查询
- `BatchGetFundNavHistory` - 批量获取历史净值
- `BatchGetFundsDetail` - 批量获取基金详情
- `GetBatchFundPerformance` - 批量业绩表现
- `GetFundDiagnosis` - 基金诊断
- `SearchFunds` - 基金搜索
- `GetPopularFund` - 热门基金

### 专业分析工具
- `getFundIndustryAllocation` - 行业配置分析
- `getBondIndicator` - 债券指标
- `getFundBrinsonIndicator` - Brinson归因
- `getMarketTimingIndicator` - 择时指标
- `GetStrategyDetails` - 策略详情

### 辅助工具
- `RenderEchart` - 图表渲染
- `RenderHtmlToPdf` - 报告生成
- `SearchFinancialNews` - 资讯搜索
- `GetCurrentTime` - 时间工具

完整工具清单请参考仓库文档。

## 快速开始

### 安装配置

1. 克隆仓库
```bash
git clone https://github.com/Chris1Wang3/Qieman-MCP.git
cd Qieman-MCP
```

2. 安装依赖
```bash
npm install
# 或
pip install -r requirements.txt
```

3. 配置环境变量
```bash
# 创建 .env 文件
cp .env.example .env

# 编辑 .env 文件，填入必要的 API 密钥
```

### 在 Claude Desktop 中使用

在 Claude Desktop 配置文件中添加：

```json
{
  "mcpServers": {
    "qieman": {
      "command": "node",
      "args": ["/path/to/Qieman-MCP/index.js"]
    }
  }
}
```

### 使用示例

**场景1：诊断基金组合**
```
我持有以下基金：易方达蓝筹精选(005827)、兴全合润(163406)、中欧时代先锋(001938)，请帮我分析组合的风险和相关性。
```

**场景2：资产配置建议**
```
我有100万资金，风险承受能力中等，希望年化收益8%左右,请帮我设计一个资产配置方案。
```

**场景3：基金筛选**
```
请帮我筛选近3年年化收益超过15%、最大回撤小于20%的偏股型基金。
```

## 技术特点

- **专业可靠**：基于且慢投顾多年积累的金融数据与分析模型
- **实时更新**：支持实时获取最新基金净值、公告与市场资讯
- **智能分析**：结合 AI 能力，提供自然语言交互式投资分析
- **可视化**：内置图表渲染与报告生成能力，结果一目了然
- **标准协议**：基于 MCP 协议，兼容 Claude Desktop、Cline 等主流 AI 工具

## 免责声明

本服务提供的所有信息、分析与建议仅供参考，不构成任何投资建议或承诺。投资有风险，决策需谨慎。使用本服务产生的任何投资损失，开发者与服务提供方不承担责任。请在充分了解风险的前提下，结合自身情况做出投资决策。

## 开源协议

MIT License

## 联系方式

- GitHub: [@Chris1Wang3](https://github.com/Chris1Wang3)
- 问题反馈: [Issues](https://github.com/Chris1Wang3/Qieman-MCP/issues)

---

**由且慢投顾提供专业金融数据支持**
