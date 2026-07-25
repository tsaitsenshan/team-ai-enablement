# 上傳規範

本文件定義一個 Skill 要達到什麼標準，才能進入 Repo。

---

## 資料夾命名規則

- 一律使用**英文**命名
- 採小寫與連字號（kebab-case），2–3 個詞為佳
- 廣為人知的技術縮寫可保留大寫：`SVG2TTF`、`TTF`、`API`
- 範例：`batch-naming`、`quality-check`、`weekly-report`、`SVG2TTF`
- 避免：日期、版本號、人名（例：`sandys-tool`、`v2-final`、`20260724-fix`）

---

## 資料夾結構

每個 Skill 資料夾須包含以下內容：

```
your-skill-name/
├── README.md          # 必須，使用說明
└── <腳本檔案>          # 實際的 script（.py / .sh / .html / .xlsx 等）
```

---

## README 必填內容

請使用根目錄 `_模版/skill-readme-template.md` 作為起點。以下欄位為必填，缺少任一項請勿上傳：

- 功能說明（含輸入、輸出）
- 輸出範例
- 適用對象
- 難度標記
- 使用方式
- 環境需求
- 已知限制
- 維護者與最後更新日期

---

## 禁止上傳的內容

以下內容嚴禁放入 Repo：

- API Key、密碼、Token 等認證資訊
- 客戶資料、合約內容
- 含有公司內部敏感資訊的檔案
- 未標示來源的第三方程式碼

若 Script 需要用到 API Key，請在 README 說明「請自行填入你的 Key」，不要把 Key 寫死在程式碼裡。

若引用了開源套件或他人的腳本，請在 README 的「第三方來源」欄位標示來源與授權方式。

---

## 上傳流程

1. 建立分支，完成資料夾與 README
2. 對照下方檢查清單自行確認
3. 發 Pull Request，指定一位同仁 review
4. Reviewer 確認必填欄位齊全、無機密資料後合併
5. 合併後於根目錄 `README.md` 的「目前可用的 Skill」表格新增一列

---

## 上傳前檢查清單

- [ ] 資料夾命名符合規範
- [ ] README.md 已填寫所有必填欄位
- [ ] 檔案內不含機密資料或 API Key
- [ ] 第三方來源已標示
- [ ] 已搜尋 Repo，確認沒有功能相似的 Skill
- [ ] 已在根目錄 README 的「目前可用的 Skill」加上自己的 Skill

---

## Skill 失效時

若你發現某個 Skill 無法正常使用，請在該 Skill 的 `README.md` 最頂部加上：

```
⚠️ 目前無法使用｜發現日期：YYYY/MM/DD
```

並於根目錄 README 的表格備註。若你是維護者本人，請盡快更新。

---

## 停用與移除

- 標記失效滿 **3 個月**未修復者，移至 `archive/` 資料夾，不直接刪除
- 移入 `archive/` 的 Skill 保留完整內容與 README，供後續參考或復原
- 每季檢視一次 `archive/`，超過 1 年且無人復原者由 Repo 維護者評估刪除
