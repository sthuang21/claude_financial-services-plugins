# /tw-screen-short

短線選股（1–5天），從上市股票中篩選符合條件的標的。

## 執行流程
1. 從 FinMind TaiwanStockInfo 取得全體上市股票清單
2. 從 TaiwanStockPrice 計算各股 5MA、20MA、成交量均量
3. 從 TaiwanStockPrice 計算日KD值
4. 從 TaiwanStockInstitutionalInvestorsBuySell 取得當日法人買賣超
5. 篩選同時符合以下條件的股票：
   - 日KD：K從20以下向上穿越D
   - 股價站上 5MA 且 5MA 向上
   - 成交量 > 20日均量 × 1.5倍
   - 外資或投信當日買超
   - 近20日均成交金額 > 3億
    - 市值 > 100億

## 輸出格式
取符合條件的前30名，依「成交量/均量比」由高到低排序。
排名 | 代號 | 名稱 | 股價 | 漲跌幅 | 日KD | 法人買超 | 量/均量比


⚠️ 本選股結果由 AI 運算產出，僅供參考，不構成投資建議。