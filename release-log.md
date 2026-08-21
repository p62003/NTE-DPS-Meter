# Changelog

## v6.3 — August 21, 2026

<details>

<summary>English</summary>

This release exists to repair what the 1.3.x game update broke: damage numbers not showing at all, only one target being recorded in multi-target fights, and gacha history capturing just the first entry per page. All three are fixed. It also adds a **Diagnostic Report** so that when a future game update breaks something, you can see immediately which part stopped lining up.

### Fix: Detection Restored After the 1.3.x Game Update

- After the game updated to 1.3.x, **damage numbers stopped appearing entirely** — fixed.
- **Only one enemy showing numbers when fighting several, and results coming and going within a single fight** — fixed. Same root cause as above: some hits were being discarded outright as they were recorded, which looked like "some targets have no numbers" and "it works, then it doesn't." In testing, multi-target fights now record roughly 1.5× as many hits.
- **Nova / Scorch / Genesis Bloom / Break had no name in the skill breakdown** — fixed. **That damage was always counted toward your DPS and total; only the name was missing.** Your totals will not change because of this fix — you can simply see these entries by name now.
- Recordings made under older game versions still read correctly; regression testing matched the previous behaviour exactly.

---

### Fix: Gacha History Recorded Only the First Entry per Page

- After the game updated to 1.3.5, paging through gacha history **captured only the first entry on each page** and quietly dropped the rest — fixed. At the time it felt like "records are coming in, but far fewer than they should be."
- **The missing records can be recovered automatically.** After updating, open your gacha history in-game and page through it once; anything missing fills itself back in, with **no manual steps**. Testing recovered 145 records.
- The weapon banner was **not affected** — it was working correctly all along.
- A useful side effect: each record now knows **which specific banner it came from** (previously only "limited" vs "standard" could be told apart). This version records it but does not yet use it in the statistics.

---

### New Feature: Diagnostic Report and Startup Self-Check

- The tray menu item "Export Network Diagnostics" is now "**Export Diagnostic Report**." It has grown from network information alone into three parts: network status, how gacha records are being captured, and data/artwork completeness — written as a **readable text file to your Desktop**.
- The gacha capture section lists each stage in order: how many arrived, how many were recognised, how many were read successfully, how many were actually stored. **When a game update breaks capture, you can see exactly which stage stopped** — attach this file when reporting and there is no need for trial and error.
- On startup the app checks that its data and artwork are complete (character portraits and full-body art, cultivation materials, gacha item icons — 264 checks in total). **It only speaks up when something is missing**, and stays completely quiet otherwise.

---

### Improvement: New Characters and Game Data Update

- **Zankou and Linko are now fully supported**: portrait, full-body art, skill names, colour, cultivation materials and bond gifts are all in place. Zankou also has an awakening background; **Linko has none yet** (the game's own data does not provide one), so that area being blank is expected.
- The skill-name table is updated to the latest game version, adding 109 newly identifiable skill names (Zankou 61 / Linko 26 / Blackbird 5). **Nothing from the previous version was lost or renamed.**
- **Linko's Traditional Chinese skill names corrected**: the game's own Traditional Chinese data has not been localised for this character yet, and using it as-is would leave this one character showing Simplified characters in a Traditional Chinese interface. It is corrected in place, and will return to the official text automatically once the game provides it.
- The skill ranking table used to show Linko under an internal code; it now shows "Linko."
- Cultivation materials, bond gifts, skill multipliers, gacha items and banners are all updated to the latest version; bond gifts and cultivation materials have **zero missing icons**.

---

### Improvement: Other Community Site Updates

- The Team Builder adds **Zankou** and **Linko**, and Kurenai's portrait has been replaced with the newer one.
- Gacha statistics add two limited weapons (Ravenous Blade, Voice of the Voyager) and two banners (Spellbound Special, Soundscape Special), all named from the game's official data.
- **Simplified Chinese text fixes**: the Traditional-to-Simplified mapping was incomplete, leaving some item names and Esper Cycle descriptions showing a mix of both scripts. With the gaps filled, the site now converts cleanly throughout.
- The protagonist "Zero" no longer carries a gender tag and simply uses the game's official name; the male and female leads remain separate entries, told apart by portrait and full-body art.
- The Team Builder's four slots now use full-bleed portraits, empty slots use dashed squares of the same size, and the layout no longer shifts when you pick your first character.

</details>

<details>

<summary>繁體中文</summary>

本版是為了修復遊戲 1.3.x 更新造成的失效而發布：傷害數字完全不顯示、打複數怪只記錄到一隻、抽卡歷史每頁只收到第一筆——三項都已修好。同時新增**診斷報告**，讓日後遊戲再改版時能立刻看出是哪裡對不上。

### 修正：遊戲 1.3.x 更新後偵測失效

- 遊戲更新到 1.3.x 之後**傷害數字完全不顯示** — 已修復。
- **打複數怪時只有一隻有數字、同一場戰鬥時好時壞** — 已修復。這與上一項同源：部分傷害在記錄階段被整筆丟掉，因此看起來像「部分目標沒數字」「一下有一下沒有」。實測多目標戰鬥的有效記錄量提升約 1.5 倍。
- **黯星／濁燃／創生花／傾陷在技能明細裡沒有名字** — 已修復。**這幾筆傷害一直都有計入 DPS 與總傷害，缺的只有名字**；修正後總數字不會改變，只是明細裡看得到它們了。
- 舊版遊戲時期留下的紀錄一樣讀得出來，回歸驗證與修正前完全一致。

---

### 修正：抽卡歷史每頁只收到第一筆

- 遊戲 1.3.5 更新後，翻抽卡歷史時**每一頁只收得到第一筆**，其餘安靜地漏掉 — 已修復。當時的感覺是「有進來，但少很多」。
- **漏掉的紀錄可以自動補回**：更新後回到遊戲裡重新開啟抽卡歷史、翻一遍，缺的會自動補齊，**不需要任何手動操作**。實測回收 145 筆。
- 武器池（限定武器）**不受影響**，原本就正常。
- 順帶取得的新資訊：每一筆紀錄現在知道自己屬於**哪一期卡池**（此前只分得出限定池與常駐池）。本版尚未用於統計，先行保留。

---

### 新功能：診斷報告與啟動自檢

- 系統匣選單的「匯出網卡診斷」更名為「**匯出診斷報告**」。內容由單純的網路資訊擴充為三段：網路狀態、抽卡紀錄的收錄狀況、資料與圖檔完整性；並以**看得懂的文字檔輸出到桌面**。
- 抽卡收錄狀況逐層列出「收到多少 → 認出多少 → 成功讀取多少 → 實際收錄多少」。**遊戲改版導致收錄失效時，可以直接看出是哪一層斷掉**；回報問題時附上這個檔案即可，不必反覆嘗試。
- 啟動時自動檢查資料與圖檔是否齊全（角色頭像立繪、養成材料、抽卡道具圖示等共 264 項）。**只在發現缺漏時才提示**，一切正常時完全不打擾。

---

### 改善：新角色與遊戲資料更新

- **殘虹與靈可正式上線支援**：頭像、全身立繪、技能名、配色、養成材料與好感度禮物全部補齊。殘虹另有覺醒背景；**靈可目前沒有覺醒背景**（遊戲官方資料尚未提供），該處留白屬正常。
- 技能名對照表更新至最新遊戲版本，可辨識的技能名新增 109 個（殘虹 61／靈可 26／黑羽 5）。對前一版已有的名稱**沒有任何遺失或更動**。
- **靈可的繁體技能名修正**：遊戲官方資料的繁中欄位對這個角色尚未在地化，直接採用會讓繁體介面只有這一個角色顯示簡體字，已就地修正為繁體字形。官方補上翻譯後會自動回到官方版本。
- 技能排行表原本把靈可顯示為內部代號，已改為顯示「靈可」。
- 養成材料、好感度禮物、技能倍率、抽卡道具與卡池同步更新至最新版本；好感度禮物與養成材料**零缺圖**。

---

### 改善：社群平台其他更新

- 隊伍搭配器新增**殘虹**與**靈可**，並換上真紅的新大頭貼。
- 抽卡統計新增兩把限定武器（弧盤噬心詭刃、弧盤遠行者之聲）與兩個卡池（攝心特刊、萬籟特刊），名稱全部取自遊戲官方資料。
- **簡體頁面的錯字修正**：繁轉簡的對照表原本不完整，部分道具名與環合反應說明長期顯示半繁半簡的壞字。本次補齊後全站零漏字。
- 主角「零」不再顯示性別標籤，一律顯示遊戲官方名；男女主仍是各自獨立的條目，靠大頭貼與立繪區分。
- 隊伍搭配器的四格改為滿版頭像，空格改用同尺寸的虛線方框，選第一個人時版面不再跳動。

</details>

<details>

<summary>简体中文</summary>

本版是为了修复游戏 1.3.x 更新造成的失效而发布：伤害数字完全不显示、打复数怪只记录到一只、抽卡历史每页只收到第一笔——三项都已修好。同时添加**诊断报告**，让日后游戏再改版时能立刻看出是哪里对不上。

### 修正：游戏 1.3.x 更新后侦测失效

- 游戏更新到 1.3.x 之后**伤害数字完全不显示** — 已修复。
- **打复数怪时只有一只有数字、同一场战斗时好时坏** — 已修复。这与上一项同源：部分伤害在记录阶段被整笔丢掉，因此看起来像「部分目标没数字」「一下有一下没有」。实测多目标战斗的有效记录量提升约 1.5 倍。
- **黯星／浊燃／创生花／倾陷在技能明细里没有名字** — 已修复。**这几笔伤害一直都有计入 DPS 与总伤害，缺的只有名字**；修正后总数字不会改变，只是明细里看得到它们了。
- 旧版游戏时期留下的纪录一样读得出来，回归验证与修正前完全一致。

---

### 修正：抽卡历史每页只收到第一笔

- 游戏 1.3.5 更新后，翻抽卡历史时**每一页只收得到第一笔**，其余安静地漏掉 — 已修复。当时的感觉是「有进来，但少很多」。
- **漏掉的纪录可以自动补回**：更新后回到游戏里重新打开抽卡历史、翻一遍，缺的会自动补齐，**不需要任何手动操作**。实测回收 145 笔。
- 武器池（限定武器）**不受影响**，原本就正常。
- 顺带取得的新信息：每一笔纪录现在知道自己属于**哪一期卡池**（此前只分得出限定池与常驻池）。本版尚未用于统计，先行保留。

---

### 新功能：诊断报告与启动自检

- 系统匣菜单的「导出网卡诊断」更名为「**导出诊断报告**」。内容由单纯的网络信息扩充为三段：网络状态、抽卡纪录的收录状况、数据与图档完整性；并以**看得懂的文本档输出到桌面**。
- 抽卡收录状况逐层列出「收到多少 → 认出多少 → 成功读取多少 → 实际收录多少」。**游戏改版导致收录失效时，可以直接看出是哪一层断掉**；回报问题时附上这个文件即可，不必反复尝试。
- 启动时自动检查数据与图档是否齐全（角色头像立绘、养成材料、抽卡道具图标等共 264 项）。**只在发现缺漏时才提示**，一切正常时完全不打扰。

---

### 改善：新角色与游戏数据更新

- **残虹与灵可正式上线支持**：头像、全身立绘、技能名、配色、养成材料与好感度礼物全部补齐。残虹另有觉醒背景；**灵可目前没有觉醒背景**（游戏官方数据尚未提供），该处留白属正常。
- 技能名对照表更新至最新游戏版本，可辨识的技能名添加 109 个（残虹 61／灵可 26／黑羽 5）。对前一版已有的名称**没有任何遗失或更动**。
- **灵可的繁体技能名修正**：游戏官方数据的繁中字段对这个角色尚未在地化，直接采用会让繁体界面只有这一个角色显示简体字，已就地修正为繁体字形。官方补上翻译后会自动回到官方版本。
- 技能排行表原本把灵可显示为内部代号，已改为显示「灵可」。
- 养成材料、好感度礼物、技能倍率、抽卡道具与卡池同步更新至最新版本；好感度礼物与养成材料**零缺图**。

---

### 改善：社群平台其他更新

- 队伍搭配器添加**残虹**与**灵可**，并换上真红的新大头贴。
- 抽卡统计添加两把限定武器（弧盘噬心诡刃、弧盘远行者之声）与两个卡池（摄心特刊、万籁特刊），名称全部取自游戏官方数据。
- **简体页面的错字修正**：繁转简的对照表原本不完整，部分道具名与环合反应说明长期显示半繁半简的坏字。本次补齐后全站零漏字。
- 主角「零」不再显示性别标签，一律显示游戏官方名；男女主仍是各自独立的条目，靠大头贴与立绘区分。
- 队伍搭配器的四格改为满版头像，空格改用同尺寸的虚线方框，选第一个人时版面不再跳动。

</details>

<details>

<summary>日本語</summary>

本バージョンは、ゲーム 1.3.x アップデートで動かなくなった機能を修復するためのリリースです。ダメージ数値がまったく表示されない、複数の敵と戦うと 1 体分しか記録されない、ガチャ履歴が 1 ページにつき 1 件しか取り込まれない——この 3 点をすべて修正しました。あわせて**診断レポート**を追加し、今後ゲームが更新された際にどこが噛み合わなくなったのかをすぐ確認できるようにしています。

### 修正：ゲーム 1.3.x アップデート後に検出できない

- ゲームが 1.3.x に更新された後、**ダメージ数値がまったく表示されない** — 修正しました。
- **複数の敵と戦うと 1 体分しか数値が出ない／同じ戦闘中でも出たり出なかったりする** — 修正しました。上記と同じ原因で、一部のダメージが記録の段階でまるごと破棄されていたため、「一部の対象に数値が出ない」「出たり出なかったりする」ように見えていました。実測では、複数対象の戦闘での有効な記録数が約 1.5 倍になりました。
- **暗星／濁燃／創生花／ブレイクがスキル詳細で名前なしになる** — 修正しました。**これらのダメージは以前から DPS と総ダメージに計上されており、欠けていたのは名前だけです。**修正によって合計値が変わることはなく、詳細で名前が見えるようになるだけです。
- 以前のゲームバージョンで取得した記録も従来どおり読み取れます。回帰確認では修正前と完全に一致しました。

---

### 修正：ガチャ履歴が 1 ページにつき 1 件しか記録されない

- ゲームが 1.3.5 に更新された後、ガチャ履歴をめくると**各ページの 1 件目しか取り込まれず**、残りは静かに取りこぼされていました — 修正しました。当時は「入ってきてはいるが、明らかに少ない」という状態でした。
- **取りこぼした記録は自動で復旧できます。** 更新後、ゲーム内でガチャ履歴をもう一度開いてめくるだけで、欠けていた分が自動的に補完されます。**手動の操作は必要ありません。** 実測で 145 件が復旧しました。
- 武器ガチャは**影響を受けていません**。もとから正常に動作していました。
- 副次的に得られた情報として、各記録が**どの復刻・特別号のものか**を保持するようになりました（従来は限定ガチャか常設かの区別のみ）。本バージョンでは記録するのみで、統計にはまだ使用していません。

---

### 新機能：診断レポートと起動時セルフチェック

- タスクトレイメニューの「ネットワーク診断をエクスポート」を「**診断レポートをエクスポート**」に変更しました。内容はネットワーク情報だけでなく、ネットワーク状態・ガチャ記録の取り込み状況・データと画像の完全性の 3 部構成になり、**読める形式のテキストファイルとしてデスクトップに出力**されます。
- ガチャの取り込み状況は「いくつ届いたか → いくつ認識できたか → いくつ読み取れたか → 実際にいくつ保存されたか」を段階ごとに表示します。**ゲーム更新で取り込みが止まったとき、どの段階で止まったかがそのまま分かります。**報告の際はこのファイルを添付いただければ、試行錯誤は不要です。
- 起動時にデータと画像が揃っているかを自動確認します（キャラクターのアイコンとイラスト、育成素材、ガチャアイテムのアイコンなど計 264 項目）。**不足が見つかったときだけ通知**し、問題がなければ何も表示しません。

---

### 改善：新キャラクターとゲームデータ更新

- **残虹とリンコに正式対応**しました。アイコン、全身イラスト、スキル名、カラー、育成素材、好感度ギフトをすべて追加しています。残虹には覚醒背景もあります。**リンコの覚醒背景は現時点で存在しません**（ゲーム側のデータに未収録のため）ので、その部分が空欄なのは正常です。
- スキル名対応表を最新のゲームバージョンに更新し、識別できるスキル名が 109 件増えました（残虹 61／リンコ 26／ブラックバード 5）。**前バージョンで表示されていた名前の消失・変更はありません。**
- **リンコの繁体字スキル名を修正**しました。ゲーム側の繁体字データがこのキャラクターについてまだローカライズされておらず、そのまま使うと繁体字表示でこのキャラクターだけ簡体字になってしまうため、字形を修正しています。ゲーム側で翻訳が提供され次第、自動的に公式の表記に戻ります。
- スキルランキング表でリンコが内部コードで表示されていた問題を修正し、「リンコ」と表示されるようになりました。
- 育成素材、好感度ギフト、スキル倍率、ガチャアイテム、ガチャ種別を最新版に同期しました。好感度ギフトと育成素材のアイコンは**欠けなし**です。

---

### 改善：コミュニティサイトのその他の更新

- パーティ編成ツールに**残虹**と**リンコ**を追加し、紅のアイコンを新しいものに差し替えました。
- ガチャ統計に限定武器 2 種（喰心刃、アストロ・コーラー）とガチャ 2 種（蠱惑特別号、万波特別号）を追加しました。名称はすべてゲーム公式データによります。
- **簡体字ページの表記修正**：繁体字から簡体字への変換表が不完全で、一部のアイテム名や異能環合の説明に繁体字と簡体字が混ざったままになっていました。今回の補完により、サイト全体で正しく変換されるようになりました。
- 主人公「ゼロ」の性別ラベルを廃止し、ゲーム公式の名称のみを表示するようにしました。男主人公・女主人公は引き続き別項目で、アイコンとイラストで区別できます。
- パーティ編成ツールの 4 枠をフル表示のアイコンに変更し、空き枠は同じサイズの破線の四角にしました。1 人目を選んだときにレイアウトがずれることはなくなりました。

</details>
