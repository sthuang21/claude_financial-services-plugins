# /tw-report [股票代號]

產出台股個股完整研究報告。

## 執行流程

### 自動取得（FinMind + 證交所）
1. 從 FinMind TaiwanStockPrice 取得近 60 日股價
2. 從 FinMind TaiwanStockFinancialStatements 取得近四季損益
3. 從 FinMind TaiwanStockMonthRevenue 取得近 12 個月營收
4. 從 FinMind TaiwanStockInstitutionalInvestorsBuySell 取得近 20 日法人動向
5. 從 FinMind TaiwanStockMarginPurchaseShortSale 取得融資融券現況
6. 從證交所 OpenAPI 取得今日即時報價

## 報告格式
1. 公司簡介與產業定位
2. 近四季財務摘要（營收、EPS、毛利率、ROE）
3. 月營收趨勢（年增率變化）
4. 技術面現況（均線位置、KD、趨勢判斷）
5. 籌碼面（三大法人、融資融券）
6. 估值分析（本益比、殖利率、股價淨值比）
7. ⚠️ 風險提示：本報告由 AI 輔助產出，僅供參考，不構成投資建議