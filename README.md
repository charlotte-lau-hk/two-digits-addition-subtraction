# 兩位數加減遊戲 · Two-Digit Add & Subtract

一個給香港小學生的兩位數加減法練習遊戲。單一 HTML 檔案，純前端（HTML + CSS + JavaScript），無需伺服器，可直接放上 GitHub Pages。

A two-digit addition & subtraction practice game for Hong Kong primary school students. A single, client-only HTML file (HTML + CSS + JavaScript) — no server, no build step, no external libraries. Ready to host on GitHub Pages.

**遊玩網址 · Play here:** `https://charlotte-lau-hk.github.io/two-digits-addition-subtraction/`
> ⬆️ 啟用 GitHub Pages 後即可使用。 · Available once GitHub Pages is enabled.

---

## 玩法 · How to play

- 先輸入名字，然後開始遊戲。 · Enter a name, then start.
- 每題四個選項，選出正確答案。 · Each question has four choices; pick the right answer.
- 每題有 **3 秒**限時（頂部的進度條會倒數）；時間到會當作答錯。 · Each question has a **3-second** limit (the top bar counts down); running out of time counts as a wrong answer.
- 答對得 **10 分**，連續答對有額外獎分。 · **10 points** per correct answer, with a bonus for streaks.
- 你有 **3 條命**（❤️），答錯 3 次遊戲結束。 · You have **3 lives** (❤️); the game ends after 3 wrong answers.
- 每題作答後會顯示對／錯 2 秒（有倒數動畫），然後自動下一題。 · Correct/wrong is shown for 2 seconds (with a countdown animation), then the next question loads.
- 也可以用鍵盤 **1–4** 作答。 · You can also answer with keys **1–4**.

### 分級 · Levels
難度會隨分數升級，共 4 級。升級時會有提示，HUD 也會顯示目前等級與距離下一級的進度條。

Difficulty levels up with your score — 4 levels in all. A banner celebrates each level-up, and the HUD shows the current level with a progress bar toward the next one.

| 等級 Level | 內容 Focus | 加減 Operations | 結果 Sums |
|---|---|---|---|
| **1** 加法 Addition | 只有加法 · addition only | 只有加法 · addition | < 100 |
| **2** 加減混合 Add & Subtract | 加減混合 · mixed | 約 55% 加 / 45% 減 | < 100 |
| **3** 減法挑戰 Subtraction | 減法為主 · more subtraction | 約 40% 加 / 60% 減 | < 100 |
| **4** 破百挑戰 Over 100 | 加入大於 100 的加法 · adds over-100 sums | 混合 · mixed | 可 ≥ 100，比例隨分數增加 · ≥ 100 allowed, more with score |

升級的分數門檻預設為 **0 / 80 / 200 / 360**（可在設定中調整）。 · The level-up score thresholds default to **0 / 80 / 200 / 360** (adjustable in settings).

### 題目 · Questions
- 只有兩位數（10–99）的加法與減法，兩個數字。 · Two-digit (10–99) addition and subtraction, two numbers only.
- 減法不會出現負數。 · Subtraction never goes negative.
- 題目由程式即時隨機產生，每次遊戲都不同。 · Questions are generated randomly in real time, so every game is different.

### 遊戲結束 · Finishing
- 顯示一張證書：學生名字、完成時間（香港時間）、用時、分數、最長連續答對。 · A certificate shows the name, timestamp (Hong Kong time), time used, score, and best streak.
- **分享到 Google Classroom** — 手機／平板會直接開啟系統分享，選 Google Classroom 即可提交圖片作功課。桌面電腦會先下載證書圖片並開啟 Classroom 視窗，請自行附上剛下載的圖片。 · **Share to Google Classroom** — on phones/tablets the native share sheet opens (pick Classroom to submit the image as homework); on desktop the image downloads first and a Classroom window opens for you to attach it.
- **下載證書圖片**（檔名與證書上的編號一致）· **Download Certificate Image** (the filename matches the certificate number printed on it)
- **我想再玩一次**（不需重新輸入名字）· **I want to try again** (no need to re-enter the name)

---

## 證書編號 · Certificate number

每張證書右上角都有一個編號（例如 `編號 No. 3F9A-2C71-8B04`），下載的圖片檔名亦與此編號一致。

Each certificate carries a number in the top-right corner (e.g. `No. 3F9A-2C71-8B04`), and the downloaded image's filename matches it.

編號的計算方法（完全在瀏覽器內）：對字串 **`yyyyMMddHHmmss,名字,分數`**（完成時的香港時間、學生名字、分數）做 **SHA-256** 雜湊，取前 12 個十六進位字元。

How it is computed (entirely in the browser): a **SHA-256** hash of the string **`yyyyMMddHHmmss,name,score`** (the Hong Kong completion time, the student's name, and the score), taking the first 12 hexadecimal characters.

### 好處 · Pros
- **同一張證書、同一個編號**：印在圖上的編號與檔名一致，老師可一眼核對兩者是否相符（不符即代表圖片被改過）。 · **One certificate, one number**: the printed number and the filename match, so a teacher can spot at a glance if they disagree (a mismatch means the image was edited).
- **提高作弊成本**：學生不能只把隨便一張圖改名交功課，也難以憑空亂作一個看似合理的編號。 · **Raises the cost of cheating**: a student can't just rename any image, nor easily invent a plausible-looking number by hand.
- **保留少量可追溯性**：編號綁定了完成時間、名字與分數。 · **Some traceability**: the number is bound to the completion time, name, and score.

### 限制 · Cons / limits
- **並非防偽**：本遊戲純前端，計算方法與程式碼都會傳送到瀏覽器。懂技術的人可用開發者工具改分數、重新計算編號，或直接用繪圖軟件偽造整張證書。 · **Not tamper-proof**: the game is client-only; the algorithm and code are all shipped to the browser. A technical user can change the score in DevTools and recompute the number, or forge the whole certificate in an image editor.
- **可重現、非隨機**：相同的秒數＋名字＋分數會得出相同編號，因此編號只證明「有人用這條公式算出這些數值」，而**不能**證明「學生真的取得該分數」。 · **Reproducible, not random**: the same second + name + score yields the same number, so it only proves "someone ran this formula on these values" — it does **not** prove "the student really earned that score".
- **沒有集中記錄／統計**：不會保存成績，也無法做班級的聚合統計。 · **No central records / statistics**: scores are not stored, and class-wide aggregate statistics are not possible.

> 想要真正可核實的成績與聚合統計，必須有伺服器端（例如以伺服器保管的密鑰做 HMAC 簽章，或由伺服器記錄成績）。本版本刻意維持純前端、零部署成本、零技術負擔，把證書編號定位為**提高作弊成本的阻嚇措施**，而非防偽保證。 · For genuinely verifiable scores and aggregate statistics you need a server side (e.g. HMAC-signing with a server-held secret, or recording results on a server). This version deliberately stays client-only — zero deployment cost, zero technical overhead — treating the certificate number as a **deterrent that raises the cost of cheating**, not a guarantee against forgery.

---

## 發佈到 GitHub Pages · Publish to GitHub Pages

1. 建立一個新的 GitHub repository（例如 `two-digits-addition-subtraction`）。 · Create a new GitHub repository (e.g. `two-digits-addition-subtraction`).
2. 上傳 `index.html` 和 `README.md`。 · Upload `index.html` and `README.md`.
3. 在 repo 的 **Settings → Pages**，把 **Source** 設為 `Deploy from a branch`，Branch 選 `main` / `(root)`，儲存。 · In **Settings → Pages**, set **Source** to `Deploy from a branch`, choose branch `main` / `(root)`, and save.
4. 等一兩分鐘，網址會是 `https://<你的用戶名>.github.io/<repo 名稱>/`。 · Wait a minute or two; the URL will be `https://<username>.github.io/<repo-name>/`.

---

## 發佈後必做一步 · One step to do after publishing

打開 `index.html`，把最上方的這一行改成你的實際網址（用於 Google Classroom 分享連結）：

Open `index.html` and change this line near the top of the `<script>` to your real URL (used for the Google Classroom share link):

```js
const GAME_URL = "https://charlotte-lau-hk.github.io/two-digits-addition-subtraction/";
```
（此連結已預先填好，如 repo 名稱不同才需修改。 · Already filled in; only change it if your repo name differs.）

### 可調校的設定 · Adjustable settings

同一段 `<script>` 頂部有幾個常數，老師可按需要修改（例如覺得 3 秒太快）：

A few constants at the top of the same `<script>` can be changed to suit your class (e.g. if 3 seconds feels too fast):

```js
const QUESTION_MS   = 3000; // 每題限時（毫秒）· time allowed per question (ms)
const FEEDBACK_MS   = 2000; // 顯示對／錯的時間（毫秒）· how long the result is shown (ms)
const POINTS        = 10;   // 每答對一題的分數 · points per correct answer
const LEVEL_MIN_SCORE = [0, 80, 200, 360]; // 升到第 1/2/3/4 級所需的分數 · score needed to reach level 1/2/3/4
```

---

## 備註 · Notes

- 完全在瀏覽器內執行，沒有收集或上傳任何資料。名字只會暫存在該裝置的瀏覽器（`localStorage`），方便下次自動填入。 · Runs entirely in the browser; nothing is collected or uploaded. The name is only kept in the device's browser (`localStorage`) to pre-fill it next time.
- 建議使用較新的 Chrome、Safari 或 Edge。手機分享圖片功能需要支援 Web Share 的瀏覽器。 · Best on a recent Chrome, Safari, or Edge. Sharing the image directly on mobile needs a browser that supports the Web Share API.
