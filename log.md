# 知識庫演進日誌 (Wiki Activity Log)

本檔案為 append-only 格式，按時間順序記錄每一次論文匯入（Ingest）、深度綜述（Synthesis）與知識庫健檢（Lint）。
格式規範：`## [YYYY-MM-DD] action | summary`

---

## [2026-11-18] init | 建立寬能隙功率半導體 (GaN / SiC / Ga2O3) LLM Wiki 知識庫架構
- 修正定位為「寬能隙與超寬能隙功率半導體元件（Wide-Bandgap & Ultra-Wide-Bandgap Power Semiconductors）」。
- 更新核心規範文件 `AGENT.md`（高壓耐壓、動態導通電阻退化、場板終端、雪崩擊穿等指標）。
- 建立分類目錄結構：`raw/`、`sources/`、`materials/`、`devices/`、`mechanisms/`、`processes/`、`metrics/`、`syntheses/`。
- 建立首頁導航 `index.md` 與功率元件橫向基準榜：`metrics/bv-vs-ron-benchmark.md`、`metrics/dynamic-ron-benchmark.md`。


## [2026-11-18] ingest | 批次收錄國立中央大學 (綦振瀛教授實驗室) 功率氮化鎵系列五篇碩士論文
- **收錄來源論文**：
  1. `sources/2019_Chen_Channel_Buffer_Epitaxy.md` (陳昱志, 2019): 通道碳雜質抑制、靠近基板超晶格過濾 71% 刃差排、剛性工程 5µm 厚膜翹曲 44µm。
  2. `sources/2024_Lu_High_Power_GaN_HEMT_Breakdown.md` (呂彥鋒, 2024): 60對超晶格+碳摻雜緩衝層 ($BV=1351\text{ V}/1600\text{ V}$, $R_{on,sp}=1.95\text{ m}\Omega\cdot\text{cm}^2$)、漸變 AlGaN 背位障壓制動態 $R_{on}$ 至 4.3x。
  3. `sources/2025_Hsu_1700V_GaN_Buffer_Layer.md` (徐紹翔, 2025): TMM 穿隧模擬破壞共振微能帶、複合週期超晶格 (M1/M2) 達成垂直耐壓 $1855\text{ V}$ ($I_{leak} < 1\ \mu\text{A/cm}^2$)、晶圓翹曲控制在 $-44\ \mu\text{m}$。
  4. `sources/2026_Wang_pGaN_Gate_Epitaxy.md` (王俊哲, 2026): 雙階 p-GaN + 超薄 UID-GaN 插入層阻斷 Mg 擴散、增強型 E-mode ($V_{th}=+0.6\text{ V}$)、$R_{on}=2.5\ \Omega\cdot\text{mm}$、順向耐壓 $11.6\text{ V}$、介面能態降低 70%。
  5. `sources/2026_Chen_Composite_Dielectric_MIS_HEMT.md` (陳思宏, 2026): 原位氧電漿退火 GaON (2nm) + ALD Al2O3 (15nm) 複合閘極、漏電壓低至 $10^{-8}\text{ mA/mm}$、順向耐壓 $21.7\text{ V}$、10 年 TDDB 壽命達 $12.0\text{ V}$、$BV_{off}=1600\text{ V}$。
- **實體與機制文件更新**：
  - 新建 `devices/p-gan-hemt.md` (p-GaN 閘極物理與 Mg 擴散抑制機制)
  - 新建 `devices/mis-hemt.md` (複合介電質 MIS-HEMT 與 TDDB 可靠度)
  - 新建 `materials/gan.md` (GaN 晶體參數、碳受體能階、MOCVD 載氣與前驅物動力學)
  - 新建 `materials/algan.md` (極化物理、臨界厚度、氣相預反應、漸變背位障)
  - 新建 `materials/substrates.md` (Si vs SiC vs Sapphire vs QST 基板、晶格/熱失配、回熔蝕刻、翹曲工程)
  - 新建 `processes/epitaxy-mocvd.md` (Aixtron CCS 系統、即時曲率監控、多層 Stoney 公式)
  - 新建 `mechanisms/current-collapse.md` (表面態虛擬閘極、GaN:C 深能階受體、背位障阻隔)
  - 新建 `mechanisms/superlattice-dislocation-filter.md` (應變誘導差排側向滑移湮滅、TMM 破壞共振穿隧)
- **橫向基準榜更新**：
  - 更新 `metrics/bv-vs-ron-benchmark.md`
  - 更新 `metrics/dynamic-ron-benchmark.md`
- **目錄更新**：
  - 更新 `index.md`，納入所有新增概念文件與文獻來源庫。

## [2026-11-19] synthesis | 產出固態專題基本知識 HTML 互動簡報投影片
- **產出檔案**：`presentations/solid-state-fundamentals.html`
- **內容涵蓋**：
  - 第 1 章：材料特徵與優質指標 (Si vs SiC vs GaN vs Ga2O3、BFOM、1D Unipolar Limit)
  - 第 2 章：纖鋅礦晶體極化物理與 2DEG 三角位能井生成機制
  - 第 3 章：矽基異質磊晶兩大先天挑戰 (17% 晶格失配、54% 熱失配、回熔蝕刻與 AlN 成核層)
  - 第 4 章：MOCVD 磊晶化學動力學 (TEGa vs TMGa $\beta$-消除反應、載氣副反應、碳背景降低至 $6.3 \times 10^{16}\text{ cm}^{-3}$)
  - 第 5 章：應變工程與超晶格缺陷過濾 (螺旋/刃差排、側向滑移湮滅、80對超晶格剛性 K 工程、翹曲 $44.24\ \mu\text{m}$)
  - 第 6 章：1700V 緩衝層與 TMM 量子穿隧抑制 (複合週期 M1/M2 破壞微能帶共振、垂直耐壓突破 $1855\text{ V}$)
  - 第 7 章：增強型 E-mode 閘極技術 (p-GaN 能帶抬升、超薄 UID-GaN 阻隔 Mg 擴散、$V_{th}=+0.6\text{ V}$、$R_{on}=2.5\ \Omega\cdot\text{mm}$)
  - 第 8 章：金氧半 MIS-HEMT 複合介電質 (原位氧電漿 GaON + ALD Al2O3、順向耐壓 $21.7\text{ V}$、10 年 TDDB 壽命達 $12.0\text{ V}$)
  - 第 9 章：動態導通電阻退化與電流崩塌 (Gate lag 虛擬閘極、Drain lag 碳陷阱、漸變 AlGaN 背位障壓制退化至 4.3x)
  - 第 10 章：固態組核心檢測儀器與方法論 (HRXRD 002/102、變溫霍爾 10K-300K、SIMS、雙脈衝動態測試)
  - 結論與展望：QST 工程基板、垂直型 GaN 元件、單晶片 Power IC。
- **功能特點**：支援鍵盤方向鍵/空白鍵翻頁、O 鍵總覽縮圖、F 鍵全螢幕、KaTeX 數學公式即時渲染、自適應響應式佈局。

## [2026-11-19] presentation | 打造 Type B 鏈式因果圖譜動態展開投影片 (Causal Graph Presentation)
- **產出檔案**：`presentations/solid-state-causal-graph-presentation.html`
- **架構特點**：
  - 左側面板：SVG 向量動態因果網絡拓撲（隨頁面切換自動生長、高亮當前路徑、支援節點點擊跳轉）。
  - 右側面板：深度物理論證與實驗數據支持（KaTeX 數學公式、Causal Ribbon 因果引導、中央大學五篇論文實測數據表、Takeaway 結論）。
  - 涵蓋 12 個核心拓撲節點：材料優值極限、2DEG 極化物理、矽基外延失配與 AlN 成核、TEGa 消除碳雜質、超晶格應力差排過濾、1700V TMM 穿隧抑制、p-GaN 閘極 UID-GaN 阻隔、GaON/Al2O3 複合介電質 10 年 TDDB、漸變背位障抑制動態 Ron、固態表徵矩陣、全域 Benchmark 與未來技術演進樹。

## [2026-11-19] report | 完成作業專屬繳交報告書 SUBMISSION_REPORT.md
- **產出檔案**：`SUBMISSION_REPORT.md`
- **內容對照**：完全符合課程評分標準 9~10 分要求：
  1. 完整主題與 300 字精要介紹。
  2. 知識庫目錄架構與 5 篇核心文獻對應連結。
  3. 教學型 HTML 簡報檔案路徑（標準版與 Type B 因果圖譜版）。
  4. 雙環 loop / graph 流程圖（Mermaid）與三個子問題詳解（重複執行、重新生成、設計理由）。
  5. 包含 4 項真實人機協作過程的異常處置與檢查紀錄表。
  6. 深度反思：明確指出「概念大綱至簡報成品」節點最易出錯，說明如何將檢查前移至逐頁手稿審查，並論述因果拓撲重構。
