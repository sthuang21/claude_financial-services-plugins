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
   - 近20日均成交金額 > 3億
   - 市值 > 100億

## 輸出格式
取符合條件的前30名，依「外資近5日累計買超」由高到低排序。
排名 | 代號 | 名稱 | 產業 | 股價 | 週KD | 外資近5日買超 | 營收年增率

⚠️ 本選股結果由 AI 運算產出，僅供參考，不構成投資建議。