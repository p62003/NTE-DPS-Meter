# Changelog

## v6.1 — July 17, 2026

<details>

<summary>English</summary>

### New Feature: Trigger-Type Bonus Damage Now Counted

Numbers popping on screen while DPS records nothing — this class of "trigger-type bonus damage" travels in a packet form that was previously unrecognizable. This version adds full support.

- **Shinku's "Instant Strike"** (the bonus hit triggered by her Watch stance) was never counted before; now every hit (including crits) is counted into DPS and report skill details in real time, verified value-by-value against recorded data (1:1 with on-screen numbers).
- Recognition is a generic mechanism, not tied to a specific character — same-type trigger damage from other characters is supported automatically as long as it uses the same form.
- Fixed occasional misses for these events.
- 999 Nights is guarded so the same damage is never double-counted.
- If you find other skills where the screen shows numbers but DPS doesn't, please report them.

---

### New Feature: Japanese Interface

- The interface now supports Japanese (full UI translation; mode names use the game's official Japanese terms), auto-selected on first launch when your OS language is Japanese.
- Data names completed with official Japanese: session/boss display names, cultivation materials, bond gifts and their shop names, gacha items and pool names, 999 Nights accessory effects.
- Japanese character names expanded to 35; characters not yet released in-game show English for now.

---

### New Feature: New Abyss Circle

- Added recognition for **Blazing Circle**; **Cresting Circle** and **Waxing Circle** are pre-registered and will be supported automatically once the game opens them.

---

### Improvement: Official Esper Resonance Names

- Elemental reaction names in skill details now use the game's official terms: Superconduct → **Hexed**, Vaporize → **Nova**, Melt → **Stain**; the English label for stagger damage is now the official **Break**.
- 59 reaction entries that used to show internal-looking codes now display proper official names — the "4_new" you may have seen is Nova, and "5_new" is Scorch.

---

### Improvement: Skill Label Fixes

- Shinku's Watch-related damage labels are renamed to "Instant Strike."
- A full scan fixed 17 more mislabeled damage entries across Kuhara, Yi, Lacrimosa, Baicang, Mint, Shinku, Nanally, and Chaos (official terms in all four languages).

---

### Improvement: Discord Login & Serial

- Discord login verification upgraded: users who logged in with the early method will be asked to log in again once at startup (one click; serials and data are unaffected).
- Serial activation adds "in use" self-healing: if a seat was left stuck by a previous session, it is reclaimed and retried automatically — no more contacting the admin.
- Activation errors now distinguish "revoked" serials (refunded payments).

---

### Improvement: Upload Consent

- Consent is now version-stamped: your existing consent carries over automatically; you'll only be asked again when the terms change.
- The consent checkbox in the announcement window can be toggled anytime, taking effect immediately.

---

### Improvement: Game Data Update

- Skill-name table updated to the latest game version; character cultivation coin costs adjusted down to official values.

---

### Fix: Updater

- Missing files or a failed updater launch no longer clears the "new version" badge; canceling or closing the updater early restores it.
- When the updater asks the main app to close, it now performs a proper shutdown handoff instead of minimizing to the tray.
- Fixed a possible timeout during the update handoff.

---

### Fix: Misc

- Various internal stability fixes.

</details>

<details>

<summary>繁體中文</summary>

### 新功能：觸發型附帶傷害入統計

畫面有跳數字、DPS 卻沒有記錄——這類「觸發型附帶傷害」走一種過去無法識別的封包形式，本版新增完整支援。

- **真紅「即瞬猛襲」**（威懾凝視觸發的附帶一擊）過去從未被統計；現在每一擊（含爆擊）即時計入 DPS 與戰報技能明細，並以實錄資料逐值驗證（與畫面數字 1:1）。
- 識別為通用機制、不綁定特定角色——其他角色的同類型觸發傷害，只要走同一形式即自動支援。
- 修復此類事件偶發漏抓的問題。
- 999 夜同步加上防護，確保同一筆傷害不會被重複計算。
- 若你發現其他「畫面有數字、DPS 沒有」的技能，歡迎回報。

---

### 新功能：日本語介面

- 介面新增日本語（全介面翻譯，模式名稱採遊戲官方日文詞）；作業系統語系為日文時，首次啟動自動選用。
- 資料名全面補齊官方日文：關卡與 Boss 顯示名、養成材料、好感度禮物與入手商店名、抽卡道具與卡池名、999 夜飾品效果名。
- 角色日文名擴充至 35 名；遊戲尚未實裝的角色暫顯英文。

---

### 新功能：軌外之境新環線

- 新增「燎原環線」識別；「浪湧環線」與「月恆環線」一併預先登記，遊戲開放即自動支援。

---

### 改善：異能環合反應正名

- 技能明細的元素反應名改用遊戲官方詞：超導→**覆紋**、蒸發→**黯星**、融化→**浸染**；傾陷的英文顯示改為官方詞 **Break**。
- 59 筆原本顯示代號的反應條目補上官方名——明細中曾出現的「4_new」即黯星、「5_new」即濁燃。

---

### 改善：技能標籤正名

- 真紅「威懾凝視」相關傷害標籤正名為「即瞬猛襲」。
- 全量掃描後再修 17 筆同型標籤：九原「致約清算」「風聲為我所用」「知曉每一條秘密」、翳「獸牙影刺」、安魂曲「惡夢」「風味變奏」、白藏「適度上班」、薄荷「極限反擊：焦糖脆片」、真紅「獨行」、娜娜莉「絕對『公正』的決鬥」「要叫大姐頭」、卡厄斯「未遲到的正義」（四語皆採官方詞）。

---

### 改善：Discord 登入與序號

- Discord 登入驗證升級：早期方式登入的用戶，啟動時會被要求重新登入一次（點登入即完成，序號與資料不受影響）。
- 序號啟用新增「使用中」自癒：席位卡在前次未正常釋放時，自動回收並重試，不再需要聯繫管理員。
- 序號啟用錯誤新增「已撤銷」提示（付款遭退款的序號）。

---

### 改善：上傳同意

- 上傳同意改為版本化記錄：已勾選的同意自動沿用，未來條款更新時才會重新徵求一次。
- 公告視窗的同意勾選隨時可勾選或取消，變更即時生效。

---

### 改善：遊戲資料更新

- 技能名對照表更新至最新遊戲版本；角色養成金幣消耗依官方新數值下修。

---

### 修正：更新器

- 更新器缺檔或啟動失敗時，不再誤清「有新版本」提示；取消或提早關閉更新器後，提示會恢復。
- 更新器要求關閉主程式時，改為正常關閉交接，不再誤縮到系統匣。
- 修正更新交接期間可能逾時的問題。

---

### 修正：其他

- 多項內部穩定性修正。

</details>

<details>

<summary>简体中文</summary>

### 新功能：触发型附带伤害入统计

画面有跳数字、DPS 却没有记录——这类「触发型附带伤害」走一种过去无法识别的封包形式，本版添加完整支持。

- **真红「即瞬猛袭」**（威慑凝视触发的附带一击）过去从未被统计；现在每一击（含爆击）即时计入 DPS 与战报技能明细，并以实录数据逐值验证（与画面数字 1:1）。
- 识别为通用机制、不绑定特定角色——其他角色的同类型触发伤害，只要走同一形式即自动支持。
- 修复此类事件偶发漏抓的问题。
- 999 夜同步加上防护，确保同一笔伤害不会被重复计算。
- 若你发现其他「画面有数字、DPS 没有」的技能，欢迎回报。

---

### 新功能：日本语接口

- 接口添加日本语（全接口翻译，模式名称采游戏官方日文词）；操作系统语系为日文时，首次启动自动选用。
- 数据名全面补齐官方日文：关卡与 Boss 显示名、养成材料、好感度礼物与入手商店名、抽卡道具与卡池名、999 夜饰品效果名。
- 角色日文名扩充至 35 名；游戏尚未实装的角色暂显英文。

---

### 新功能：轨外之境新环线

- 添加「燎原环线」识别；「浪涌环线」与「月恒环线」一并预先登记，游戏开放即自动支持。

---

### 改善：异能环合反应正名

- 技能明细的元素反应名改用游戏官方词：超导→**覆纹**、蒸发→**黯星**、融化→**浸染**；倾陷的英文显示改为官方词 **Break**。
- 59 笔原本显示代号的反应条目补上官方名——明细中曾出现的「4_new」即黯星、「5_new」即浊燃。

---

### 改善：技能标签正名

- 真红「威慑凝视」相关伤害标签正名为「即瞬猛袭」。
- 全量扫描后再修 17 笔同型标签：九原「致约清算」「风声为我所用」「知晓每一条秘密」、翳「兽牙影刺」、安魂曲「恶梦」「风味变奏」、白藏「适度上班」、薄荷「极限反击：焦糖脆片」、真红「独行」、娜娜莉「绝对『公正』的决斗」「要叫大姐头」、卡厄斯「未迟到的正义」（四语皆采官方词）。

---

### 改善：Discord 登录与序号

- Discord 登录验证升级：早期方式登录的用户，启动时会被要求重新登录一次（点登录即完成，序号与数据不受影响）。
- 序号激活添加「使用中」自愈：席位卡在前次未正常释放时，自动回收并重试，不再需要联系管理员。
- 序号激活错误添加「已撤销」提示（付款遭退款的序号）。

---

### 改善：上传同意

- 上传同意改为版本化记录：已勾选的同意自动沿用，未来条款更新时才会重新征求一次。
- 公告窗口的同意勾选随时可勾选或取消，变更即时生效。

---

### 改善：游戏数据更新

- 技能名对照表更新至最新游戏版本；角色养成金币消耗依官方新数值下修。

---

### 修正：更新器

- 更新器缺档或启动失败时，不再误清「有新版本」提示；取消或提早关闭更新器后，提示会恢复。
- 更新器要求关闭主程序时，改为正常关闭交接，不再误缩到系统匣。
- 修正更新交接期间可能逾时的问题。

---

### 修正：其他

- 多项内部稳定性修正。

</details>

<details>

<summary>日本語</summary>

### 新機能：トリガー型追加ダメージの計測

画面には数字が出ているのに DPS には記録されない——この種の「トリガー型追加ダメージ」は、これまで認識できなかった形式で送られていました。本バージョンで完全に対応しました。

- **真紅の「刹那の猛撃」**（特定状態から発動する追加の一撃）はこれまで一度も計測されていませんでした；現在はすべてのヒット（クリティカル含む）が DPS と戦闘レポートのスキル詳細にリアルタイムで反映され、実録データで一つずつ検証済みです（画面の数字と 1:1）。
- 認識は汎用機構であり特定のキャラクターに紐づきません——他のキャラクターの同型トリガーダメージも、同じ形式であれば自動的に対応します。
- この種のイベントがまれに取りこぼされる問題を修正しました。
- 九百九十九夜にも同時に保護を追加し、同一のダメージが二重に計算されないようにしました。
- 他にも「画面に数字が出るのに DPS に乗らない」スキルを見つけた場合は、ぜひご報告ください。

---

### 新機能：日本語インターフェース

- インターフェースが日本語に対応しました（UI 全体を翻訳、モード名はゲーム公式の日本語表記を採用）；OS の言語が日本語の場合、初回起動時に自動で選択されます。
- データ名も公式日本語で全面的に整備：セッションとボスの表示名、育成素材、好感度ギフトと入手ショップ名、ガチャアイテムとバナー名、九百九十九夜のアクセサリー効果名。
- 日本語のキャラクター名は 35 名まで拡充；ゲーム未実装のキャラクターは暫定的に英語表記となります。

---

### 新機能：軌道外領域の新しい環状線

- **焦熱の環状線**の認識に対応しました；**激流の環状線**と**月恒の環状線**も事前に登録済みで、ゲームで開放され次第、自動的に対応します。

---

### 改善：エスパー環合反応の名称を公式表記に統一

- スキル詳細の元素反応名がゲーム公式の用語になりました：超電導 → **覆紋**、蒸発 → **暗星**、溶解 → **浸染**；ブレイクダメージの英語表記も公式用語の **Break** に変更しました。
- これまでコード表記のままだった 59 件の反応項目に公式名を補完しました——詳細で見かけた「4_new」は暗星、「5_new」は濁燃です。

---

### 改善：スキルラベルの名称修正

- 真紅の威嚇状態に関連するダメージラベルを「刹那の猛撃」に統一しました。
- 全件スキャンにより、さらに 17 件の同型ラベルを修正：九原「誓約の清算」「噂話の利用価値」「全ての秘密を知る者」、翳「影獣牙突」、レクイエム「悪夢」「フレーバー変奏」、白蔵「適度出勤」、ミント「極限反撃：キャラメルクランチ」、真紅「独歩」、ナナリ「絶対『公正』な決闘」「姉御と呼ぶべし」、カオス「逃れられぬ正義」（4 言語すべて公式用語を採用）。

---

### 改善：Discord ログインとシリアルキー

- Discord ログイン認証をアップグレードしました：旧方式でログインしていた方は、起動時に一度だけ再ログインを求められます（クリックするだけで完了、シリアルキーとデータに影響はありません）。
- シリアルキーの有効化に「使用中」の自動復旧を追加：前回のセッションで枠が解放されないまま固まっていた場合、自動的に回収して再試行します——管理者への連絡は不要になりました。
- 有効化エラーに「取り消し済み」の案内を追加しました（支払いが返金されたシリアルキー）。

---

### 改善：アップロード同意

- アップロード同意をバージョン管理方式に変更：既にご同意いただいている内容はそのまま引き継がれ、今後は規約が更新されたときのみ再度確認します。
- アナウンスウィンドウの同意チェックはいつでもオン／オフでき、変更は即座に反映されます。

---

### 改善：ゲームデータ更新

- スキル名対照表を最新のゲームバージョンに更新しました；キャラクター育成のコイン消費も公式の新数値に合わせて下方修正しました。

---

### 修正：アップデーター

- アップデーターのファイル欠損や起動失敗時に、「新しいバージョンがあります」の通知を誤って消さないよう修正しました；アップデーターをキャンセルまたは早期に閉じた場合、通知は元に戻ります。
- アップデーターがメインプログラムの終了を要求する際、トレイに誤って最小化されず、正常に終了して引き継ぐようになりました。
- 更新の引き継ぎ中にタイムアウトする可能性があった問題を修正しました。

---

### 修正：その他

- 内部の安定性に関する複数の修正。

</details>