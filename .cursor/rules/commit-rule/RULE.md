---
alwaysApply: true
---
## Git Commit Message 規範（必遵守）

1. 格式：`<type>：<繁體中文描述>`，冒號須使用全形 `：`。type 僅能擇一：add、fix、restruct、test、doc、delete。
2. 描述：必須全繁體中文，建議 10～30 字，需說清改動與影響，避免空泛字眼（如 try、change、update）。
3. 禁則：不得自創 type、不得一次寫多個 type、不得以英文為描述內容。
4. 不符規範者請修改後再提交，CI/PR 守門將拒絕不合格式的 commit。
5. 提交方式：因全形字元需以 UTF-8 編碼，Windows 環境請用 `git commit -F <檔案>` 或 Git Bash，避免 PowerShell 直接 `-m` 造成亂碼。


### 範例
- add：支援 Markdown 條列解析為卡片
- fix：分頁超出範圍時回傳空清單並提示
- delete：移除已廢棄的 foo API 文檔路由

### 反例（不接受）
- add:add feature（描述不是繁中且冒號為半形）
- change：update（描述空泛且 type 不在清單內）
- feat：新增功能（type 不在清單內）