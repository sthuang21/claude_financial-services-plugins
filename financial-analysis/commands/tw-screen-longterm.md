# /tw-screen-longterm

長線選股（6個月以上），從上市股票中篩選優質標的。

## 執行流程
1. 從 FinMind TaiwanStockInfo 取得全體上市股票清單
2. 從 TaiwanStockPrice 確認月線（240MA）方向
3. 從 TaiwanStockFinancialStatements 計算近三年 ROE、EPS 趨勢
4. 從 TaiwanStockDividend 計算現金殖利率
5. 從 TaiwanStockBalanceSheet 計算負債比
6. 篩選同時符合以下條件的股票：
   - 月線（240MA）向上
   - 近三年 ROE 均 > 15%
   - 近三年 EPS 穩定成長
   - 現金殖利率 > 5%
   - 負債比 < 50%
   - 近20日均成交金額 > 3億
   - 市值 > 100億

## 輸出格式
取符合條件的前30名，依「近三年平均ROE」由高到低排序。
排名 | 代號 | 名稱 | 產業 | 股價 | 殖利率 | ROE | EPS趨勢 | 負債比 | 綜合評分（高 / 中 / 低）

⚠️ 本選股結果由 AI 運算產出，僅供參考，不構成投資建議。