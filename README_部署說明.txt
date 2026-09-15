致生涯．理未來｜正式修正版

【採用 A 方案】
topicEnded 只由人工決定：
- TRUE：此主題服務已結束
- FALSE / 空白：仍視為進行中
不依服務日期自動結案。

【Records 正式欄位】
id | year | studentId | topic | scoreX | scoreY | scoreZ | topicEnded | counselor | location | notes

【Sessions 正式欄位】
record_id | date | timeStart | timeEnd | headcount | teacherFilled

【本版修正】
1. counselor/location/notes 若工作表缺欄位，GAS 會自動補齊。
2. 專業人員缺值時前端顯示「未設定」，不再顯示 undefined。
3. scoreX/Y/Z 的空白、null、undefined、未填都視為「未填」。
4. 待結案 KPI 與案件狀態使用同一套缺問卷判定。
5. 日期固定 yyyy-MM-dd；時間固定 HH:mm。
6. favicon 統一放 ./assets/，並加版本參數避免舊快取。
7. 登入頁 ICON 與頁首一致使用「致」。
8. 管理員密碼完全未修改。

【GAS 部署】
1. Apps Script 開啟目前專案。
2. 用 Code.gs 全部取代目前程式碼。
3. 儲存。
4. 點「部署」→「管理部署」→ 編輯目前部署 → 建立新版本 → 部署。
5. Web App URL 不需要換，前端仍使用原本 URL。

【GitHub Pages】
把以下內容上傳到 repository 根目錄：
- index.html
- site.webmanifest
- assets/ 整個資料夾

舊檔 favicon.ico、favicon-*.png 若在根目錄，可刪除，避免混淆。

【舊資料】
已確定結束的案件：在 Records 的 topicEnded 改 TRUE。
未確認是否結束：維持 FALSE 或空白。
