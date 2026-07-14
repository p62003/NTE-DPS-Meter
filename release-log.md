# Changelog

## v6.0 — July 13, 2026

<details>

<summary>English</summary>

### New Feature: Discord Login for All Users + Serial Ownership Binding

Startup identity verification has been upgraded from a "sponsor activation prerequisite" to "login for all users," with serial ownership binding established in the cloud.

- **Startup Login** — Both free and sponsor users complete a one-time Discord login at startup (can be done right from the Discord button in the announcement window); users who have already linked Discord are unaffected.
- **Serial Ownership** — A serial claims its owner on first activation; afterward only the owner can re-activate it, preventing serials from being stolen and used by others.
- The announcement window's Discord login was rebuilt into a single just-in-time flow (cancel or login both return to the announcement, no longer exiting the app), with a persistent "Re-link Discord" button.

---

### New Feature: Full Support for 999 Nights

The new continent "999 Nights" goes from completely unrecognized to full report support.

- Correctly identifies the character used in 999 Nights.
- Correctly calculates your outgoing damage in 999 Nights and filters out incoming damage from monsters (also fixes related calculation in normal modes).
- Reports are correctly categorized as "999 Nights" (previously mis-saved as Free Combat), with a dedicated icon.

---

### New Feature: New Instances and Abyss Route Recognition

- **Howling Circle** — New abyss route recognition, completing all 12 stations (upper/lower halves).
- **Gloaming Circle** — New abyss route recognition.
- **Debt Collector** — New weekly boss recognition with a dedicated icon.
- **HeheBear (Misty Tracking)** — New danger commission recognition.

---

### New Feature: New Character Data

- Added full data for **Chaos**, **Shinku**, and **Iroi** (avatar, full-body art, awakening background, cultivation, skill multipliers, skill names, gacha limited items), plus cultivation data for **Zero (Male)**.
- Skill name table updated to the latest game version, adding new character skill names and official names for 999 Nights accessory relic effects.
- Gacha adds 2 weapons, 2 pools, and several outfits.
- Bond preference data completed for 20 characters.

---

### New Feature: Automatic Report Upload

- **Free Users** — Reports auto-upload in the background as soon as they're saved (pending reports are also backfilled at startup); the upload button now shows "Auto-Uploaded."
- **Sponsor Users** — A new "Auto Upload" toggle in the context menu (off by default).
- Upload consent moved to a one-time confirmation in the announcement window, removing the per-upload popup.

---

### New Feature: Combat Detail Dual Tabs

The combat detail panel adds "Cast / Hit" dual tabs:

- **Cast** — Lists skill names (all three languages) and cast counts per skill.
- **Hit** — Per-hit timing, damage, current target HP, and kill events.

---

### New Feature: Notification Dots

When a new report is saved or a new version is available, the interface guides you to the relevant feature with red dots.

- **New Report** — Red dots on the main window report button, sidebar arrow, tray icon, and the "Report Manager" context menu item; cleared when you open the report sidebar or report manager.
- **New Version** — Red dots on the main window menu button, tray icon, the "Announcement" context menu item, and the announcement window's "Check for Updates" button; cleared when the updater launches.

---

### New Feature: OS Language Auto-Detection on First Launch

On first launch, the interface language is now chosen automatically based on your Windows system language (Traditional Chinese / Simplified Chinese / English); users who have manually changed the language always keep their choice.

(Behavior change: existing users who never manually changed the language will auto-switch to the matching language on the next launch under an English or Simplified Chinese system.)

---

### New Feature: Analytics Platform Sponsor Purchase Page

The analytics platform adds a purchase page for overseas users to sponsor directly.

- After paying via PayPal or Ko-fi, a serial is generated automatically and sent by email (6 / 11 / 15 USD for 30 / 60 / 90 days).
- Taiwan users see a Discord contact prompt.

---

### New Feature: Analytics Platform Sponsor Slots

- Five public pages (Home / Rankings / Compositions / Gacha / Connect) add a sponsor slot above the FAQ; the first sponsor, ExitLag, is now live.

---

### Improvements

**Desktop Interface**
- Main window's three panels now have text outline and shadow for better readability.
- Announcement window redesign: sectioned cards (Update / Links / Serial), links as a standalone card, update content in version capsule tabs (shows one version at a time to avoid clutter across consecutive updates).
- Context menu: checkable items no longer close the menu when clicked; language switched to a three-language radio submenu; added "Show Overlay" (reopen if accidentally closed); "Main Window" renamed "Show Main Window"; "More Data (Sponsor)" renamed "Community Platform" and moved below "Gacha Records"; removed "Copy Device ID" and the right-click sponsor toggle (serial activation unified in the announcement window).
- After activating or deactivating a serial, the dashboard and compare mode sponsor gate releases or restores instantly, without reopening the window.
- The report sidebar and manager add character / target dual dropdown filters (with avatars) and an "Uploadable" quick-filter chip; wider sidebar, per-report upload buttons (sponsor), and a larger expand arrow.
- Main window nav bar adds a "Reports" button (toggles the report sidebar).
- Combat detail, ECG, and appearance-frequency cards add draggable scrollbars; the ECG hints that you can hold Ctrl + scroll to zoom.
- Opens the leaderboard page automatically after a successful manual upload; the report "Stage" column renamed "Target."

**Updater**
- Downloads support interrupted-resume and three retries; a failed update auto-recovers instead of being left half-applied; double-launch is prevented; updates run entirely in the background without freezing the UI.
- Missing or corrupt config now exits with a clear error instead of silently falling back.
- Fixed the online program showing an old version number.

**Analytics Platform**
- Rankings always show real public data (blur removed), add a "Teammates" avatar column, and default to sorting by max DPS; improved mixed-leaderboard ordering, enlarged top-3 numbers, and per-row range bars.
- Luck Leaderboard adds a "Luck Rate" column and ranks by it.
- Purchase page visuals aligned site-wide, sponsor color unified to purple, nav renamed "Sponsor."

**Gacha**
- Automatically detects and removes duplicate gacha records at startup, correcting the inflated pity distance (the over-90 artifact) they caused with zero user action; community cloud data repaired in sync.

---

### Fixes

**Serial & Payment**
- Serial verification moved to a custom domain, fixing "cannot connect to verification server" for users in China (the old domain was blocked by the firewall). ⚠️ Older builds still hit the old domain — update to this version to take effect.
- Fixed serials getting stuck after a manual deactivation (already-stuck serials need a customer-service reset).
- Fixed a PayPal case of "paid but no serial received," and fixed a case of incorrect serial issuance.
- Fixed a case where a serial could be wrongly marked as permanently invalid.
- Hardened upload identity verification to prevent name spoofing on leaderboards and forged sponsor status.
- Fixed a double-payment risk on the purchase page, adding fault tolerance and a "do not pay twice" prompt.

**Desktop**
- Danger commission exits now end and save the report correctly.
- Fixed jitter when exiting a single-boss fight, ensuring one fight produces one report.
- Improved auto-upload crash resilience — an unexpected shutdown no longer leaves behind corrupt reports.
- Fixed a wrong background color block on the dashboard appearance-statistics card.
- Fixed white lines in the report sidebar and white edges on target icons.
- Fixed the main program failing to start in certain cases.

**Updater**
- Fixed the updater getting stuck at "Applying update" after completion.
- Fixed a loop that repeatedly prompted for updates when there were no changes.

</details>

---

<details>

<summary>繁體中文</summary>

### 新功能：全用戶 Discord 登入驗證與序號擁有權綁定

啟動時的身份驗證從「贊助啟用前置」升級為「全用戶登入」，並在雲端建立序號擁有權綁定。

- **啟動登入** — 免費與贊助用戶啟動時皆需完成一次 Discord 登入（可在公告視窗的 Discord 按鈕就地完成）；已綁定 Discord 的用戶不受影響。
- **序號擁有權** — 序號首次啟用時認領擁有者，之後僅擁有者本人能再次啟用，防止序號被他人盜用。
- 公告視窗的 Discord 登入重構為單一即時流程（取消或登入都回到公告，不再退出程式），並提供常駐「重新連結 Discord」按鈕。

---

### 新功能：999 夜完整支援

新大陸「999 夜」從完全無法識別升級為完整戰報支援。

- 正確識別 999 夜中使用的角色。
- 正確計算你在 999 夜的輸出傷害，並排除怪物對你造成的傷害干擾（同時修正一般模式的相關計算）。
- 戰報正確歸類為「999 夜」（先前誤存為自由戰鬥），並配專屬圖標。

---

### 新功能：新副本與深淵路線識別

- **呼嘯環線** — 新增深淵路線識別，補齊全 12 站上下半。
- **晦冥環線** — 新增深淵路線識別。
- **討債人** — 新增週本 Boss 識別與專屬圖標。
- **桀桀熊（迷霧追蹤）** — 新增危險委託識別。

---

### 新功能：新角色資料

- 新增 **卡厄斯**、**真紅**、**伊洛伊** 完整角色資料（頭像、立繪、覺醒背景、養成、技能倍率、技能名、抽卡限定），並補齊 **零（男）** 養成資料。
- 技能名稱表更新至遊戲最新版本，新增新角色技能名，並為 999 夜飾品遺物補上正式名稱。
- 抽卡新增 2 把武器、2 個卡池與多件時裝。
- 好感度偏好資料補齊至 20 名角色。

---

### 新功能：戰報自動上傳

- **免費用戶** — 戰報存檔即自動於背景上傳（啟動時亦會補傳先前未上傳的戰報），上傳按鈕改顯示「已自動上傳」。
- **贊助用戶** — 右鍵選單新增「自動上傳」開關（預設關閉）。
- 上傳同意條款移至公告視窗一次性確認，不再每次上傳彈窗。

---

### 新功能：戰鬥細節雙分頁

戰鬥細節面板新增「施放 / 擊中」雙分頁：

- **施放** — 依技能列出三語技能名與施放次數。
- **擊中** — 逐次命中的時間、傷害、當前目標血量與擊殺事件。

---

### 新功能：紅點提示

新戰報入庫或有新版本可更新時，介面會以紅點指引你走到對應功能。

- **新戰報** — 主視窗戰報按鈕、側邊欄箭頭、系統匣圖示與右鍵選單「戰報管理」皆顯示紅點，開啟戰報側欄或戰報管理即清除。
- **新版本** — 主視窗選單按鈕、系統匣圖示、右鍵選單「公告」與公告視窗「檢查更新」皆顯示紅點，啟動更新器即清除。

---

### 新功能：首次啟動自動偵測系統語系

首次啟動時，介面語言會依 Windows 系統語系自動選擇（繁中 / 简中 / English）；曾手動變更過語言的用戶永遠維持自己的選擇。

（行為變更：老用戶若從未手動改過語言，在英文或简中系統下次啟動時會自動切換為對應語言。）

---

### 新功能：分析平台贊助購買頁

分析平台新增購買頁，海外用戶可自助贊助。

- 透過 PayPal 或 Ko-fi 付款後自動產生序號並以 email 寄送（6 / 11 / 15 USD 對應 30 / 60 / 90 天）。
- 台灣用戶顯示 Discord 洽詢提示。

---

### 新功能：分析平台贊助商版位

- 五個公開頁面（首頁 / 排行榜 / 配對率 / 抽卡 / 連結）的 FAQ 上方新增贊助商版位，首個贊助商 ExitLag 已上線。

---

### 改善

**桌面介面**
- 主視窗三面板文字加入描邊與陰影，提升可讀性。
- 公告視窗改版：分區卡片（更新內容 / 連結 / 序號）、連結獨立成卡、更新內容以版本膠囊分頁（連續多版更新時一次只顯示一版，解決壅擠）。
- 右鍵選單：勾選項點選後選單不再關閉、語言改為三語直選子選單、新增「展開浮窗」（誤關可重開）、「主視窗」更名「展開主視窗」、「更多數據（贊助）」更名「社群平台」並移至「抽卡紀錄」下方；移除「複製 Device ID」與右鍵啟停贊助（序號啟停統一至公告視窗）。
- 序號啟用或停用後，儀表板與比對模式的贊助鎖即時解除或恢復，不需重開視窗。
- 戰報側邊欄與管理視窗新增角色 / 目標雙下拉篩選（帶頭像）與「可上傳」快篩膠囊；側邊欄加寬、新增逐份上傳按鈕（贊助）、展開箭頭放大。
- 主視窗導覽列新增「戰報」按鈕（開關戰報側邊欄）。
- 戰鬥細節、心電圖與使用頻率卡新增可拖曳捲軸；心電圖非波峰處提示可長按 Ctrl + 滾輪縮放。
- 手動上傳成功後自動開啟排行榜頁；戰報「關卡」欄更名為「目標」。

**更新器**
- 下載支援中斷續傳與三次重試、更新失敗會自動復原不會套用到一半、防止重複開啟，更新全程於背景執行不卡 UI。
- 設定檔缺失或損毀時明確報錯退出，不再靜默回退。
- 修正線上程式顯示舊版號的問題。

**分析平台**
- 排行榜永遠公開真實資料（移除模糊遮罩），新增「同場隊友」頭像欄，預設以最大 DPS 排序；混合榜排序優化、前三名數字放大、範圍條逐列正規化。
- 幸運榜新增「幸運率」欄位並改以幸運率排名。
- 購買頁視覺對齊全站、贊助色統一為紫色、導覽列更名「贊助」。

**抽卡**
- 啟動時自動偵測並移除重複的抽卡紀錄，修正因重複紀錄造成的保底距離異常（超過 90 的虛高假象，用戶零操作）；社群雲端資料同步修復。

---

### 修正

**序號與金流**
- 序號驗證改用自訂網域，修復中國用戶「無法連接驗證伺服器」的問題（原網域遭防火牆阻斷）。⚠️ 舊版程式仍連舊網域，須更新至本版才生效。
- 修正手動取消啟用後序號卡死無法再啟用的問題（卡死的既有序號需聯繫客服重置）。
- 修正 PayPal 付款在特定情況下「已付款但未收到序號」的問題，並修正特定情況下的序號誤發。
- 修正某些情況下序號被誤置為永久失效的問題。
- 強化上傳身份驗證，防止冒用他人名稱顯示於排行榜或偽造贊助資格。
- 修正購買頁重複付款風險，付款流程加入容錯與「請勿重複付款」提示。

**桌面**
- 危險委託離場時正確結束並存檔戰報。
- 修正單一 Boss 戰離場時的抖動，確保一場戰鬥只產生一份報告。
- 提升自動上傳的崩潰韌性，程式意外關閉不再留下損毀的戰報。
- 修正儀表板出場統計卡片的背景色塊錯誤。
- 修正戰報側邊欄的白線與目標圖標白邊問題。
- 修正特定情況下主程式無法啟動的問題。

**更新器**
- 修正更新完成後停在「正在套用更新」不結束的問題。
- 修正無變更時反覆提示更新的問題。

</details>

---

<details>

<summary>简体中文</summary>

### 新功能：全用户 Discord 登录验证与序号拥有权绑定

启动时的身份验证从「赞助激活前置」升级为「全用户登录」，并在云端创建序号拥有权绑定。

- **启动登录** — 免费与赞助用户启动时皆需完成一次 Discord 登录（可在公告窗口的 Discord 按钮就地完成）；已绑定 Discord 的用户不受影响。
- **序号拥有权** — 序号首次激活时认领拥有者，之后仅拥有者本人能再次激活，防止序号被他人盗用。
- 公告窗口的 Discord 登录重构为单一即时流程（取消或登录都回到公告，不再退出程序），并提供常驻「重新链接 Discord」按钮。

---

### 新功能：999 夜完整支持

新大陆「999 夜」从完全无法识别升级为完整战报支持。

- 正确识别 999 夜中使用的角色。
- 正确计算你在 999 夜的输出伤害，并排除怪物对你造成的伤害干扰（同时修正一般模式的相关计算）。
- 战报正确归类为「999 夜」（先前误存为自由战斗），并配专属图标。

---

### 新功能：新副本与深渊路线识别

- **呼啸环线** — 添加深渊路线识别，补齐全 12 站上下半。
- **晦冥环线** — 添加深渊路线识别。
- **讨债人** — 添加周本 Boss 识别与专属图标。
- **桀桀熊（迷雾追踪）** — 添加危险委托识别。

---

### 新功能：新角色数据

- 添加 **卡厄斯**、**真红**、**伊洛伊** 完整角色数据（头像、立绘、觉醒背景、养成、技能倍率、技能名、抽卡限定），并补齐 **零（男）** 养成数据。
- 技能名称表更新至游戏最新版本，添加新角色技能名，并为 999 夜饰品遗物补上正式名称。
- 抽卡添加 2 把武器、2 个卡池与多件时装。
- 好感度偏好数据补齐至 20 名角色。

---

### 新功能：战报自动上传

- **免费用户** — 战报存盘即自动于背景上传（启动时亦会补传先前未上传的战报），上传按钮改显示「已自动上传」。
- **赞助用户** — 右键菜单添加「自动上传」开关（缺省关闭）。
- 上传同意条款移至公告窗口一次性确认，不再每次上传弹窗。

---

### 新功能：战斗细节双分页

战斗细节面板添加「施放 / 击中」双分页：

- **施放** — 依技能列出三语技能名与施放次数。
- **击中** — 逐次命中的时间、伤害、当前目标血量与击杀事件。

---

### 新功能：红点提示

新战报入库或有新版本可更新时，界面会以红点指引你走到对应功能。

- **新战报** — 主窗口战报按钮、侧边栏箭头、系统匣图标与右键菜单「战报管理」皆显示红点，打开战报侧栏或战报管理即清除。
- **新版本** — 主窗口菜单按钮、系统匣图标、右键菜单「公告」与公告窗口「检查更新」皆显示红点，启动更新器即清除。

---

### 新功能：首次启动自动侦测系统语系

首次启动时，界面语言会依 Windows 系统语系自动选择（繁中 / 简中 / English）；曾手动变更过语言的用户永远维持自己的选择。

（行为变更：老用户若从未手动改过语言，在英文或简中系统下次启动时会自动切换为对应语言。）

---

### 新功能：分析平台赞助购买页

分析平台添加购买页，海外用户可自助赞助。

- 通过 PayPal 或 Ko-fi 付款后自动产生序号并以 email 寄送（6 / 11 / 15 USD 对应 30 / 60 / 90 天）。
- 台湾用户显示 Discord 洽询提示。

---

### 新功能：分析平台赞助商版位

- 五个公开页面（首页 / 排行榜 / 配对率 / 抽卡 / 链接）的 FAQ 上方添加赞助商版位，首个赞助商 ExitLag 已上线。

---

### 改善

**桌面界面**
- 主窗口三面板文本加入描边与阴影，提升可读性。
- 公告窗口改版：分区卡片（更新内容 / 链接 / 序号）、链接独立成卡、更新内容以版本胶囊分页（连续多版更新时一次只显示一版，解决壅挤）。
- 右键菜单：勾选项点击后菜单不再关闭、语言改为三语直选子菜单、添加「展开浮窗」（误关可重开）、「主窗口」更名「展开主窗口」、「更多数据（赞助）」更名「社群平台」并移至「抽卡纪录」下方；移除「拷贝 Device ID」与右键启停赞助（序号启停统一至公告窗口）。
- 序号激活或停用后，仪表板与比对模式的赞助锁即时解除或恢复，不需重开窗口。
- 战报侧边栏与管理窗口添加角色 / 目标双下拉筛选（带头像）与「可上传」快筛胶囊；侧边栏加宽、添加逐份上传按钮（赞助）、展开箭头放大。
- 主窗口导览列添加「战报」按钮（开关战报侧边栏）。
- 战斗细节、心电图与使用频率卡添加可拖曳滚动条；心电图非波峰处提示可长按 Ctrl + 滚轮缩放。
- 手动上传成功后自动打开排行榜页；战报「关卡」栏更名为「目标」。

**更新器**
- 下载支持中断续传与三次重试、更新失败会自动复原不会套用到一半、防止重复打开，更新全程于背景运行不卡 UI。
- 设置档缺失或损毁时明确报错退出，不再静默回退。
- 修正在线程序显示旧版号的问题。

**分析平台**
- 排行榜永远公开真实数据（移除模糊遮罩），添加「同场队友」头像栏，缺省以最大 DPS 排序；混合榜排序优化、前三名数字放大、范围条逐列归一化。
- 幸运榜添加「幸运率」字段并改以幸运率排名。
- 购买页视觉对齐全站、赞助色统一为紫色、导览列更名「赞助」。

**抽卡**
- 启动时自动侦测并移除重复的抽卡纪录，修正因重复纪录造成的保底距离异常（超过 90 的虚高假象，用户零操作）；社群云端数据同步修复。

---

### 修正

**序号与金流**
- 序号验证改用自订网域，修复中国用户「无法连接验证服务器」的问题（原网域遭防火墙阻断）。⚠️ 旧版程序仍连旧网域，须更新至本版才生效。
- 修正手动取消激活后序号卡死无法再激活的问题（卡死的既有序号需联系客服重置）。
- 修正 PayPal 付款在特定情况下「已付款但未收到序号」的问题，并修正特定情况下的序号误发。
- 修正某些情况下序号被误置为永久失效的问题。
- 强化上传身份验证，防止冒用他人名称显示于排行榜或伪造赞助资格。
- 修正购买页重复付款风险，付款流程加入容错与「请勿重复付款」提示。

**桌面**
- 危险委托离场时正确结束并存盘战报。
- 修正单一 Boss 战离场时的抖动，确保一场战斗只产生一份报告。
- 提升自动上传的崩溃韧性，程序意外关闭不再留下损毁的战报。
- 修正仪表板出场统计卡片的背景色块错误。
- 修正战报侧边栏的白线与目标图标白边问题。
- 修正特定情况下主程序无法启动的问题。

**更新器**
- 修正更新完成后停在「正在套用更新」不结束的问题。
- 修正无变更时反复提示更新的问题。

</details>