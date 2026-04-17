# /tw-chips [股票代號]

深度分析個股籌碼狀況。

## 執行流程
1. 從 FinMind TaiwanStockInstitutionalInvestorsBuySell
   取得近 20 日三大法人每日明細
2. 從 FinMind TaiwanStockMarginPurchaseShortSale
   取得融資融券近 20 日餘額變化
3. 從 FinMind TaiwanStockHoldingSharesPer
   取得最新股權分散表
4. 從 FinMind TaiwanDailyShortSaleBalances
   取得借券狀況

## 輸出內容
- 法人態度評估（偏多 / 偏空 / 觀望）
- 融資水位風險評估
- 大戶持股趨勢（增加 / 減少）
- 整體籌碼評分與觀察重點
- ⚠️ 僅供參考，不構成投資建議