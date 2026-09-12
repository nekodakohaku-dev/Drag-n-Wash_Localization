DragNWash XUnity Dialogue Layout Fix 0.1.0

針對 Yarn 的對話排版相容修正。翻譯仍由 BepInEx/Translation/zh-TW/Text 內的 XUnity TXT 提供。
Yarn 在設定對話文字後，會再次呼叫 GetTextInfo(英文原文)。這個方法會重新設定文字並產生網格，覆蓋 XUnity 已顯示的中文。
此修正在 Line Presenter 範圍內，先使用 XUnity 的 TryTranslate 快取查詢替換 GetTextInfo 的參數。
不呼叫線上翻譯，不建立字型、不掃描字型資源、不修改遊戲檔案。

已通過編譯與靜態介面核對；仍需遊戲內測試。
成功啟動時會記錄 Dialogue layout fix loaded。
第一次成功處理對話時會記錄 Applied XUnity translation before Yarn's GetTextInfo layout pass。
移除本資料夾即可移除此修正。不要重新啟用舊版 DragNWash.ZhTW。
