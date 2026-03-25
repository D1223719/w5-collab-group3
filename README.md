# 第五週 Pull Request 協作練習

這是第五週的分組作業，練習完整的 Pull Request 協作流程。
**重點不只是寫程式，而是 PR 描述、Code Review 與回應 review 的過程。**

---

## 基本資料

| 項目        | 填寫           |
| ----------- | -------------- |
| 組別        | 第三組  |
| 組員        | 黃國傑  楊永蘭  蔡秉倫  辛晴  薛帆凱 |
| GitHub Repo | w5-collab-group3 |
| 報告日期    | 2025 /03 /25 |

---

## 快速開始

**組長**

1. Fork 該 repo → 命名為 `w5-collab-第X組` → **Create fork**
2. Settings → Branches → Add rule：`main`，勾選 **Require PR + 2 approvals**
3. Settings → Collaborators → 邀請所有組員
4. 把 repo URL 告訴組員

**組員**

```bash
git clone https://github.com/組長帳號/w5-collab-第X組.git
cd w5-collab-第X組
git checkout -b feature/member-a   # 依角色選擇
```

---

## Review Comment 範例

每個 PR 至少需要 **2 位成員 approve** 才能 merge。
Review 時留下有意義的 comment，以下是常見的寫法：

**✅ 肯定 / Approve 常用語**

```
LGTM!
```

```
LGTM! 邏輯很清楚，merge 沒問題 👍
```

```
Ship it! 🚀
```

```
Nice work! 時間戳格式選得很好，HH:MM 簡潔又夠用。
```

```
Looks good to me, 就這樣 merge 吧。
```

**💬 提問或確認意圖**

```
nit: 這個變數名稱可以再清楚一點嗎？（nit = nitpick，小建議，不影響 approve）
```

```
Esc 清空是清空輸入框還是整個對話？PR 描述可以補一下。
```

```
這裡用 querySelectorAll 是有考慮到未來擴充嗎？好奇問一下 😄
```

```
optional: 可以加 localStorage 記住 dark mode 狀態，但不一定要這次做。
```

**🔧 建議修改**

```
nit: `d` 這個變數名不太好懂，建議改成 `chatBox`。
```

```
這裡有重複的程式碼，可以抽成一個 function，會更好維護。
```

```
minor: clearChat 沒有 confirm 視窗，使用者可能會不小心清掉，要不要加個確認？
```

**⚠️ 指出問題（Request changes）**

```
這裡如果輸入是空字串會壞掉，需要先加個判斷再 merge。
```

```
WIP? 這個 function 好像還沒實作完，先確認一下？
```

```
blocking: 這個會影響其他功能，需要修一下才能 merge。
```

---

**常見縮寫對照**

| 縮寫     | 全文               | 意思               |
| -------- | ------------------ | ------------------ |
| LGTM     | Looks Good To Me   | 沒問題，可以 merge |
| nit      | Nitpick            | 小建議，不強制修改 |
| WIP      | Work In Progress   | 還沒做完           |
| PTAL     | Please Take A Look | 請幫我看一下       |
| TBD      | To Be Determined   | 待確認             |
| optional | —                 | 可做可不做的建議   |
| blocking | —                 | 必須修才能 merge   |

> **記住**：review 是討論，不是批判。指出問題時說明原因，建議修改方向，而不是直接否定。

---

## PR 描述規範（每個 PR 都要填）

```markdown
## 做了什麼
- （說明新增或修改了什麼）

## 如何測試
1. （步驟一）
2. （步驟二）

## 截圖
（附上修改後的畫面截圖）
```

---

## 完整協作流程

```
組長：Fork 模板 → 設 Branch Protection → 邀請組員
  ↓
各組員：clone → 建分支 → 完成任務 → push → 開 PR（填完整描述）
  ↓
組長：Review PR → 留 comment → Approve
  ↓
組員：回應 comment → 修改 → re-push
  ↓
組長：Merge（解決 conflict）
  ↓
全組：git pull origin main → 確認成果
```

---

## 一、協作分工

| 組員姓名 | 負責分支 | 主要修改內容 | PR 連結 | 是否完成 |
| -------- | -------- | ------------ | ------- | -------- |
| 楊永蘭 |D1245806 | 新增登入功能以及儲存歷史對話紀錄分支 | https://github.com/D1223719/w5-collab-group3/pull/1 | ✅ |
| 蔡秉倫 |feature/search-conversation| 新增搜尋對話功能 | https://github.com/D1223719/w5-collab-group3/pull/3 | ✅ |
| 辛晴 | feature/xin | 完成背景愛心動畫與 UI 配色更改  |https://github.com/D1223719/w5-collab-group3/pull/4 |✅|
| 薛帆凱 |feature/member-sailboat | 新增讀取TXT檔內容的功能 | https://github.com/D1223719/w5-collab-group3/pull/2 | ✅ |


---

## 二、截圖紀錄

### 2-1 PR 列表截圖（必填）

> 截圖：GitHub repo → Pull requests，顯示所有 PR 的狀態（open / merged）

<img width="1847" height="798" alt="image" src="https://github.com/user-attachments/assets/4f3b0ef7-576d-48b2-981e-3583abb6932a" />


---

### 2-2 PR 描述截圖（必填）

> 截圖：其中一個 PR 的描述頁面，顯示完整的「做了什麼 / 如何測試」內容

<img width="1720" height="962" alt="image" src="https://github.com/user-attachments/assets/35858d00-d55b-4f3f-a1a3-f217ddfb73b5" />
<img width="1070" height="562" alt="image" src="https://github.com/user-attachments/assets/03893e45-b881-47f4-b0b4-06d9d36735a4" />
<img width="1063" height="572" alt="image" src="https://github.com/user-attachments/assets/e7ecfcb0-9c73-4e33-9f57-32089bc5848b" />


---

### 2-3 Code Review 截圖（必填）

> 截圖：Files changed 頁面，顯示 inline comment 的留言

<img width="1276" height="538" alt="image" src="https://github.com/user-attachments/assets/f57b7b3d-4d2e-41a9-b77c-11079fdc0daf" />


---

### 2-4 Merge 成功截圖（必填）

> 截圖：某個 PR 頁面顯示「Merged」紫色標籤

<img width="1684" height="584" alt="image" src="https://github.com/user-attachments/assets/d3715e84-5057-43a9-b6fe-3fe394794a9a" />


---

### 2-5 最終成果截圖（必填）

> 截圖：用瀏覽器打開 `index.html`，顯示所有功能整合完成的畫面

<img width="1912" height="1070" alt="image" src="https://github.com/user-attachments/assets/159ba71b-a721-45cf-a841-7b9c814d9861" />
<img width="1911" height="983" alt="image" src="https://github.com/user-attachments/assets/44bbb1a2-28f1-4d49-9b24-bf9afb2941b2" />


---

## 三、遇到的問題與解決方式

**問題 1：**
遇到3個分支有conflict
解決方式：
先將錯誤部分整合一起，再修正錯誤
---

**問題 2：**
從github 上 clone專案的程式碼，antigravity上沒顯示已更改的程式碼

解決方式：
記得儲存
---

## 四、個人心得

> 每位組員各寫 2–3 句，說明這週對 PR / Code Review 的理解或感想

** 黃國傑：我藉由組長的任務分配，學習到了如何去有效率的討論並修正錯誤，也了解到要當組長不是那麼輕鬆的事，不僅要了解整體的流程，也要去留意組員們交上來的程式碼有沒有造成conflict，也要想辦去commit組員給出建議修改、整合並確認整體的chatbox功能是否完整，今天的實作確實讓我學習到很多。 **

** 楊永蘭：我透過實作「登入功能」與「歷史對話儲存」，為系統建立了穩固的安全與持久化基礎：這兩項核心功能的完成，確保了使用者資料的安全性，並讓對話內容能夠跨 Session 延續，是將單機工具轉型為成熟 Web 應用的關鍵步驟。 **

**蔡秉倫：我認為目前的開發節奏非常明確且高效：新增「搜尋對話功能」，讓我感覺正逐步建立起一個邏輯清晰、功能完備的對話應用程式架構，展現了良好的專案規劃能力。**

**薛帆凱：我透過實作讀取 TXT 內容的功能，為系統建構了穩固的數據輸入基礎：這不僅讓程式具備處理外部文本的能力，更為後續的對話分析與資料檢索預留了發揮空間，是我在完善後端資料流處理中關鍵的一步。**

**辛晴：我同步推進了「背景動畫」與「UI 配色」的優化，致力於提升產品的整體視覺吸引力：在確保功能穩定的同時，我也注重介面的美感與操作直覺性，透過精細的色彩調整與動態效果，讓使用者在操作時能獲得更愉悅的感官體驗。**

---

## 五、自評與互評

| 評分項目            | 分數（1–5） | 說明 |
| ------------------- | ------------ | ---- |
| PR 描述完整度        | 4   |對於功能實作邏輯有清晰的描述，讓團隊能快速掌握技術重點。|
| Review comment 品質 | 4   | 能精準指出代碼中的潛在問題，並在 UI 優化上給予極具建設性的改善建議。|
| 回應 review 的態度  | 5  | 面對修改建議時回應迅速且態度積極，大幅提升協作效率。 |
| 最終成果完整度      | 5  | 對成果感到滿意，他成功兼顧了後端功能的穩定性與前端 UI 的美感，讓專案呈現極高完整度。 |

這週覺得最有挑戰的是？

- [v] 寫 PR 描述
- [v] 給 Code Review
- [v] 回應 review 並修改
- [v] 解決 Merge Conflict
- [] 其他：＿＿＿

---

*報告由全組共同完成，commit 到 main 後繳交。*
