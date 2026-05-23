**[English](README.md)** | **繁體中文** | **[简体中文](README_CN.md)**

# NTE DPS Meter

**Neverness to Everness (NTE)** 非侵入式即時傷害統計工具。

透過被動封包分析即時計算戰鬥數據 — **不修改記憶體、不竄改封包、不具備任何自動化功能**。

---

## 支持專案

如果這個工具對你有幫助，歡迎贊助支持持續開發：

### ☕ Ko-fi — 推薦

[![Support on Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/rj0217)

直接連結：[ko-fi.com/rj0217](https://ko-fi.com/rj0217)

贊助超過 6 美金，請讓我們知道，我們希望能主動向您奉上贊助者序號（Pro 功能）以表謝意。

### 🪙 加密貨幣 — USDT / USDC (BEP20 / BSC network)

```
0x55c439b27807415e80452f59ba00fee3441a802d
```

贊助超過 6 美金，請讓我們知道，我們希望能主動向您奉上贊助者序號（Pro 功能）以表謝意。

### 💬 聯絡方式

- **Discord**: https://discord.gg/nbTMDCpvrB
- **Email**: dont.stop.ha@gmail.com

---

## 功能

### 即時 DPS 浮窗

置頂透明卡片，圓形角色頭像 + 呼吸光環 + 五行即時數據（傷害、命中、DPS、HPS、ECT）。戰鬥時自動展開，5 秒無命中自動收回。戰鬥中滑鼠自動穿透，不影響遊戲操作。

![Overlay Idle](images/overlay_idle_EN.png)
![Overlay Combat](images/overlay_combat_EN.png)

### 角色辨識

自動識別當前操作角色，支援全部已上線角色。4 人隊伍中每個角色獨立追蹤傷害。

### 戰報與戰報管理

按 **F6** 重置統計 — 當前戰鬥自動存為戰報。從右鍵選單開啟戰報管理，可依傷害範圍篩選、排序、上傳至社群平台或刪除。

![Report Manager](images/report_manager_EN.png)

### 社群分析平台 — [ntedpsmeter.com](https://ntedpsmeter.com)

匯集社群上傳的戰鬥數據：

- **角色傷害排行榜** — 依戰鬥時長分 Tier（1min / 3min / 6min / 9min），顯示中位數 + 最大值 + 區間
- **角色配對矩陣** — 視覺化角色搭配採用率熱力圖（贊助者限定）
- **Connect 綁定** — 貼上 Device ID 或 Analytics Token 即可在網頁查看個人數據
- **三語網站** — EN / 繁體中文 / 简体中文
- **隱私友善** — 上傳前須明確同意，數據匿名化

### 主視窗

一目了然的全隊傷害貢獻 — 角色排名欄 + 命中細節欄雙欄佈局。所有資料保存在本地。

![Main Window](images/main_window_EN.png)

### 戰報比對（贊助者）

A/B 並排對比不同隊伍配置，顯示傷害與 DPS 差異摘要。

![Compare Mode](images/compare_mode_EN.png)

### 其他功能

- **快捷鍵** — F6 重置、Alt+D 浮窗、Alt+E 主視窗；可完全自訂
- **網卡選擇** — 手動切換網路介面，適用加速器/VPN 環境；持續支援 ExitLag
- **三語系介面** — 繁體中文 / 简体中文 / English，即時切換
- **系統匣常駐** — 不佔工作列
- **自動更新** — 從右鍵選單檢查更新

---

## 免費 vs 贊助者

| 功能 | 免費 | 贊助者 |
|------|------|--------|
| DPS 浮窗 | ✔ | ✔ |
| 角色辨識 | ✔ | ✔ |
| 戰報管理（存檔/篩選/上傳/刪除） | ✔ | ✔ |
| 快捷鍵（浮窗/重置，可自訂） | ✔ | ✔ |
| 網卡選擇 | ✔ | ✔ |
| 社群排行榜 | ✔ | ✔ |
| 主視窗（排名+細節+戰報回顧） | ✔ | ✔ |
| 戰報比對（A/B 並排） | — | ✔ |
| 角色配對矩陣 | — | ✔ |

贊助者序號是支持開發的感謝回饋，不是訂閱服務。每組序號有效期 **30 天**。免費功能永遠不受限制。

---

## 安裝與使用

### 系統需求
- Windows 10 / 11
- [Npcap](https://npcap.com/#download)（安裝時勾選「Install Npcap in WinPcap API-compatible Mode」）

### 快速開始
1. 下載最新版本 → [Releases](../../releases)
2. 解壓縮後 **右鍵 → 以系統管理員身份執行**
3. 啟動 NTE — 首次命中後浮窗自動顯示
4. 按 **F6** 重置並存檔戰報
5. 右鍵浮窗或系統匣圖標開啟完整選單

![Context Menu](images/context_menu_EN.png)

### 預設快捷鍵

| 快捷鍵 | 功能 |
|--------|------|
| `F6` | 重置統計並存檔戰報 |
| `Alt + D` | 顯示/隱藏浮窗 |
| `Alt + E` | 顯示/隱藏主視窗 |

快捷鍵可從右鍵選單 → 快捷鍵設定自訂。

![Hotkey Settings](images/hotkey_settings_EN.png)

---

## 常見問題

**Q: 浮窗沒有反應？**
A: 確認已以系統管理員身份執行，且 Npcap 已正確安裝（WinPcap 相容模式）。

**Q: 開了加速器後抓不到封包？**
A: 右鍵浮窗 →「選擇網卡」，手動切換到正確的網路介面。

![Interface Select](images/interface_select_EN.png)

**Q: 顯示的傷害數值準確嗎？**
A: 數值直接來自遊戲客戶端發送的戰鬥封包，與遊戲內部計算一致。

**Q: 為什麼一直跳防毒偵測？**
A: 本程式尚未購買 EV 程式碼簽章憑證，Windows Defender 可能將其標記為不明程式。請將程式所在資料夾加入排除清單：

桌面右鍵 → 顯示設定 → 隱私權與安全性 → Windows 安全性 → 病毒與威脅防護 → 管理設定 → 向下滾動找到「排除項目」→ 新增排除項目 → 資料夾 → 選擇程式所在目錄

---

## 免責聲明

本程式僅供技術交流與戰鬥數據分析使用。透過被動封包分析計算戰鬥數據，不修改遊戲記憶體、不竄改遊戲通訊封包，亦不具備任何自動化操作功能。

本工具為第三方輔助工具，與 Hotta Studio、Perfect World 無任何關聯。儘管採非侵入式設計，但官方對「第三方輔助程式」定義不一。使用前請自行評估 NTE 官方政策。開發者不負擔因使用本工具導致帳號受限或任何損失的法律責任或補償義務。執行程式即視為同意此聲明。

---

## 聯絡資訊

- **Discord**: https://discord.gg/nbTMDCpvrB
- **Email**: dont.stop.ha@gmail.com

請見上方[支持專案](#支持專案)段落了解贊助管道。
