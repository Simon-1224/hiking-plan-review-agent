# 登山計畫審查 AI Agent
Hiking Plan Review Agent

結合路線、氣象、裝備與補給的行前檢核系統。使用者提交既有登山計畫，Agent 取得適用資料、執行分析與領域規則，回傳附證據的問題及修改建議。

**目前階段：Proposal。** 本儲存庫收錄提案、簡報與系統設計；尚未完成可執行產品、API 串接或成效實驗。

## Proposal 交付
- [Proposal Document（Word）](docs/proposal.docx)
- [Proposal Document（Markdown）](docs/proposal.md)
- [Proposal PPT](slides/proposal.pptx)
- [DESIGN.md](DESIGN.md)
- [交付與需求對照](docs/DELIVERABLES.md)
- [合成輸入範例](data/examples/plan.synthetic.json)

## 系統能力
1. 將計畫解析成結構化欄位，對關鍵缺值追問。
2. 取得有時間與空間適用範圍的官方資料。
3. 以程式分析路線、步程、裝備與補給。
4. 以版本化領域規則檢查跨項目矛盾。
5. 呈現問題、證據、資料不足與修正後的重新審查。

## 範圍
第一版規劃支援 3 條建檔路線的單日與兩天一夜非技術登山計畫。實際路線、模型與核閱者尚待確認。
輸出為行前決策支援，不能視為現場安全證明或出發許可。

## 規劃技術
前端 React／TypeScript；後端 Python FastAPI；SQLite；JSON/YAML 規則；LLM 工具呼叫與文件檢索。選型為提案，尚未鎖定版本。

## 後續開發
以 DESIGN.md 的模組、資料契約、驗收條件及變更紀錄為依據。完成實作後再補上安裝與啟動指令，避免將尚不存在的程式當作可執行服務。

## 維護
修改來源規則、API、欄位或評估方法時，同步更新 DESIGN.md、提案及簡報。真實隊員資料、聯絡資訊、密鑰與未授權 GPX 不應提交至公開儲存庫。
