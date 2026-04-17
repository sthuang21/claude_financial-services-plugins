# 台股選股 Skill

## 資料來源
所有選股條件皆透過 FinMind API 取得，範圍限定上市股票（TWSE）。

## 選股條件庫

### 基本面條件
- EPS 年增率 > 20%（成長股）
- 近四季 ROE > 15%
- 現金殖利率 > 5%
- 月營收年增率連續三個月為正
- 負債比 < 50%
- 毛利率 > 30%

### 技術面條件
- 短線：日KD 低檔交叉（K從20以下向上穿越D）
- 波段：週KD 低檔交叉 + 站上月線（20MA）
- 長線：月線（240MA）向上 + 季線（60MA）多頭排列
- 突破：股價突破近 52 週高點，成交量放大 1.5 倍以上

### 籌碼面條件
- 外資連續買超 5 日以上
- 投信連續買超 3 日以上
- 外資＋投信同步買超（雙法人認同）
- 融資餘額減少但股價上漲（健康上漲）
- 股權分散表大戶（400張以上）持股比例增加

## 週期對應選股策略

### 短線（1–5天）
主要條件：
1. 日KD 低檔交叉
2. 外資或投信當日買超前20名
3. 成交量突破 20 日均量 1.5 倍
4. 股價站上 5MA 且 5MA 向上

### 波段（1–3個月）
主要條件：
1. 週KD 低檔交叉
2. 站上月線（20MA）且月線向上
3. 外資連續買超 5 日
4. 月營收年增率連續三個月正成長
5. 近四季 EPS 優於去年同期

### 長線（6個月以上）
主要條件：
1. 月線（240MA）向上
2. ROE 連續三年 > 15%
3. 現金殖利率 > 5%
4. 負債比 < 50%
5. 近三年 EPS 穩定成長

## FinMind 對應資料集
- 股價與均線：TaiwanStockPrice
- 本益比/本淨比：TaiwanStockPER
- 月營收：TaiwanStockMonthRevenue
- 財務報表：TaiwanStockFinancialStatements
- 三大法人：TaiwanStockInstitutionalInvestorsBuySell
- 融資融券：TaiwanStockMarginPurchaseShortSale
- 股權分散：TaiwanStockHoldingSharesPer
- 上市股票清單：TaiwanStockInfo