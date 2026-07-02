# 人生資源儀表板 Life Resource Instrument

六條人生資源曲線(體力、流體智力、知識、淨資產、剩餘時間、自由時間)+ 目標回推定位器。
輸入年齡、目標金額、目前淨資產、預期報酬率,即時判定資產進度(落後/符合/超前)並自動調整各階段優先順序。

## 使用

直接開啟 GitHub Pages 網頁,或本地打開 `index.html` 即可(單檔、無 build 步驟,依賴 CDN 載入 React 18 / Recharts / Tailwind / Babel standalone)。

## 修改

所有邏輯都在 `index.html` 內:

- `CURVES`:六條曲線的控制點(年齡→水準),改數字即改曲線
- `wealthEngine()`:方法三應達曲線模型(25歲起、固定年投入、恆定報酬)
- `computePriorities()`:優先順序權重規則

改完 push 到 main,Pages 約一分鐘後自動更新。

## 模型假設與限制

- 曲線為一般化模型,非個人預測
- 計算器忽略通膨(建議輸入實質報酬率)、假設投入固定
- 非投資建議
