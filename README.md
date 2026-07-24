# 兩位數加減遊戲 · Two-Digit Add & Subtract

一個給香港小學生的兩位數加減法練習遊戲。單一 HTML 檔案，純前端（HTML + CSS + JavaScript），無需伺服器，可直接放上 GitHub Pages。

A two-digit addition & subtraction practice game for Hong Kong primary school students. A single, client-only HTML file (HTML + CSS + JavaScript) — no server, no build step, no external libraries. Ready to host on GitHub Pages.

**遊玩網址 · Play here:** `https://charlotte-lau-hk.github.io/two-digits-addition-subtraction/`
> ⬆️ 啟用 GitHub Pages 後即可使用。 · Available once GitHub Pages is enabled.

---

## 玩法 · How to play

- 先輸入名字，然後開始遊戲。 · Enter a name, then start.
- 每題四個選項，選出正確答案。 · Each question has four choices; pick the right answer.
- 答對得 **10 分**，連續答對有額外獎分。 · **10 points** per correct answer, with a bonus for streaks.
- 你有 **3 條命**（❤️），答錯 3 次遊戲結束。 · You have **3 lives** (❤️); the game ends after 3 wrong answers.
- 每題作答後會顯示對／錯 2 秒，然後自動下一題。 · Correct/wrong is shown for 2 seconds, then the next question loads.
- 也可以用鍵盤 **1–4** 作答。 · You can also answer with keys **1–4**.

### 題目 · Questions
- 只有兩位數（10–99）的加法與減法，兩個數字。 · Two-digit (10–99) addition and subtraction, two numbers only.
- 加法總和不超過 99；減法不會出現負數。 · Sums never exceed 99; subtraction never goes negative.
- 難度會逐漸提升（後段題目一定要進位／退位）。 · Difficulty ramps up (later questions always need carrying / borrowing).

### 遊戲結束 · Finishing
- 顯示一張證書：學生名字、完成時間（香港時間）、用時、分數、最長連續答對。 · A certificate shows the name, timestamp (Hong Kong time), time used, score, and best streak.
- **分享到 Google Classroom** — 手機／平板會直接開啟系統分享，選 Google Classroom 即可提交圖片作功課。桌面電腦會先下載證書圖片並開啟 Classroom 視窗，請自行附上剛下載的圖片。 · **Share to Google Classroom** — on phones/tablets the native share sheet opens (pick Classroom to submit the image as homework); on desktop the image downloads first and a Classroom window opens for you to attach it.
- **下載證書圖片** · **Download Certificate Image**
- **再玩一次**（不需重新輸入名字）· **Try Again** (no need to re-enter the name)
- **換名字** · **Change Name**

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

---

## 備註 · Notes

- 完全在瀏覽器內執行，沒有收集或上傳任何資料。名字只會暫存在該裝置的瀏覽器（`localStorage`），方便下次自動填入。 · Runs entirely in the browser; nothing is collected or uploaded. The name is only kept in the device's browser (`localStorage`) to pre-fill it next time.
- 建議使用較新的 Chrome、Safari 或 Edge。手機分享圖片功能需要支援 Web Share 的瀏覽器。 · Best on a recent Chrome, Safari, or Edge. Sharing the image directly on mobile needs a browser that supports the Web Share API.
