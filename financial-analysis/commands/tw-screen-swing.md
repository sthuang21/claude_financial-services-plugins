# /tw-screen-swing

波段選股（1–3個月），從上市股票中篩選符合條件的標的。

## 執行流程
1. 從 FinMind TaiwanStockInfo 取得全體上市股票清單
2. 從 TaiwanStockPrice 計算週KD、月線（20MA）方向
3. 從 TaiwanStockInstitutionalInvestorsBuySell 計算外資近5日累計買賣超
4. 從 TaiwanStockMonthRevenue 計算近三個月營收年增率
5. 從 TaiwanStockFinancialStatements 比較近四季 EPS 年增率
6. 篩選同時符合以下條件的股票：
   - 週KD 低檔交叉（K從30以下向上穿越D）
   - 股價站上月線（20MA）且月線向上
   - 外資近5日累計買超為正
   - 月營收年增率近三個月均為正
   - 近四季 EPS 優於去年同期

## 輸出格式
列出符合條件股票，每檔附上：
- 股票代號、名稱、產業
- 目前股價
- 週KD數值
- 外資近5日買超金額
- 近三個月營收年增率
- 近四季EPS趨勢

⚠️ 本選股結果由 AI 運算產出，僅供參考，不構成投資建議。