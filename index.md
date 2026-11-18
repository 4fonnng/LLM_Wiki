# 知識庫總目錄 (Index)

本知識庫專注於**寬能隙與超寬能隙功率半導體（Wide-Bandgap & Ultra-Wide-Bandgap Power Semiconductors: GaN, SiC, $\text{Ga}_2\text{O}_3$ 等）**，記錄元件耐壓物理、磊晶製程、高壓開關特性、動態退化機制與對比指標。

---

## 快速導航 (Quick Links)
- [[metrics/bv-vs-ron-benchmark|耐壓與比導通電阻基準榜 (BV vs Ron,sp)]]
- [[metrics/dynamic-ron-benchmark|動態導通電阻退化基準榜 (Dynamic Ron)]]
- [[log|變更日誌 (Changelog / Log)]]

---

## 1. 材料體系與基板 (Materials & Substrates)
- **半導體材料**
  - [[materials/gan|GaN 材料特性與磊晶物理 (GaN Material Properties & Growth Physics)]]
  - [[materials/algan|AlGaN 材料與極化異質結構 (AlGaN & Polarization Heterostructures)]]
  - [[materials/substrates|異質磊晶基板特性與應變匹配 (Substrates: Si vs SiC vs Sapphire vs QST)]]
- **介電層與鈍化**
  - [[materials/sin-passivation|SiNx 鈍化層 (LPCVD / PECVD)]]
  - [[devices/mis-hemt|GaON / Al2O3 複合介電質閘極堆疊]]

---

## 2. 功率元件架構 (Power Device Architectures)
- **橫向高電子遷移率電晶體 (Lateral HEMTs)**
  - [[devices/p-gan-hemt|增強型 p-GaN 閘極 HEMT (E-mode HEMT & Mg Diffusion Control)]]
  - [[devices/mis-hemt|金氧半高電子遷移率電晶體 (MIS-HEMT & 10-Year TDDB Reliability)]]
  - [[devices/cascode-hemt|Cascode 結構 HEMT]]
- **垂直功率元件 (Vertical Power Devices)**
  - [[devices/vertical-trench-mosfet|垂直溝槽閘極 MOSFET (Trench MOSFET)]]
  - [[devices/planar-mosfet|垂直平面閘極 MOSFET (Planar MOSFET)]]

---

## 3. 介面物理、可靠度與機制 (Physics & Mechanisms)
- [[mechanisms/superlattice-dislocation-filter|超晶格缺陷過濾與穿隧抑制機制 (Superlattice Dislocation Filter & TMM)]]
- [[mechanisms/current-collapse|動態導通電阻與電流崩塌機制 (Dynamic Ron & Current Collapse)]]
- [[mechanisms/buffer-trapping|緩衝層摻雜與陷阱效應 (Carbon CN Deep Acceptor Trapping)]]
- [[mechanisms/vth-stability|增強型閘極穩定性與經時介電崩潰 (Vth Stability & TDDB)]]

---

## 4. 製程技術與耐壓終端 (Processes & Termination)
- [[processes/epitaxy-mocvd|MOCVD 磊晶工藝與應變工程 (Aixtron CCS, Precursors & In-situ Curvature)]]
- [[processes/field-plate-design|場板電場調控設計 (Field Plate Engineering)]]
- [[devices/mis-hemt|複合介電層製程 (原位低損傷氧電漿 GaON + ALD Al2O3)]]
- [[devices/p-gan-hemt|超薄 UID-GaN 擴散阻擋層製程]]

---

## 5. 跨文獻橫向指標與綜述 (Metrics & Syntheses)
- **橫向評測榜**
  - [[metrics/bv-vs-ron-benchmark|耐壓與比導通電阻對比榜 (BV vs Ron,sp)]]
  - [[metrics/dynamic-ron-benchmark|動態導通電阻退化榜 (Dynamic Ron / Current Collapse)]]
- **專題報告與簡報 (Presentations & Syntheses)**
  - [[SUBMISSION_REPORT.md|作業繳交完整報告書 (含 Loop/Graph 流程圖、檢查紀錄與反思)]]
  - [[presentations/solid-state-causal-graph-presentation.html|固態專題基本知識：鏈式因果圖譜動態展開簡報 (Type B Interactive Graph Presentation)]]
  - [[presentations/solid-state-fundamentals.html|固態專題基本知識：寬能隙氮化鎵功率元件物理、磊晶與可靠度全覽 (HTML 標準簡報)]]

---

## 6. 收錄論文文獻庫 (Sources Catalog)

本知識庫已批次收錄國立中央大學電機工程學系（綦振瀛教授實驗室）功率氮化鎵系列研究成果：

1. **2019** | [[sources/2019_Chen_Channel_Buffer_Epitaxy|陳昱志 - 矽基氮化鎵高電子遷移率電晶體 通道層與緩衝層之成長與材料特性分析]]
   - *關鍵成果*: TEGa 前驅物消除通道碳雜質 (10K 遷移率 $28,000$)；靠近基板之超晶格將刃差排降低 71%；80 對超晶格剛性工程達成 6 吋 $5.0\ \mu\text{m}$ 厚膜且翹曲僅 $44.24\ \mu\text{m}$。
2. **2024** | [[sources/2024_Lu_High_Power_GaN_HEMT_Breakdown|呂彥鋒 - 高功率氮化鎵高電子遷移率電晶體崩潰特性優化研究]]
   - *關鍵成果*: GaN:C 緩衝層 ($1.8 \times 10^{19}\text{ cm}^{-3}$) + 60 對超晶格垂直場強達 $2.28\text{ MV/cm}$；元件耐壓達 $1351\text{ V} / >1600\text{ V}$ ($R_{on,sp} = 1.95\text{ m}\Omega\cdot\text{cm}^2$)；漸變 AlGaN 背位障 (150nm) 將動態 $R_{on}$ 退化壓制至 4.30 倍。
3. **2025** | [[sources/2025_Hsu_1700V_GaN_Buffer_Layer|徐紹翔 - 6 吋矽基板上沉積 1700 V 氮化鎵高電子遷移率電晶體之緩衝層研究]]
   - *關鍵成果*: 穿透矩陣法 (TMM) 破壞超晶格共振穿隧；高場漏電上升斜率減緩 10%；垂直崩潰電壓達到 **$1855\text{ V}$** ($I_{leak} < 1\ \mu\text{A/cm}^2$)；晶圓翹曲精準控制在 $-44\ \mu\text{m}$。
4. **2026** | [[sources/2026_Wang_pGaN_Gate_Epitaxy|王俊哲 - p型氮化鎵閘極磊晶結構對增強型氮化鎵高電子遷移率電晶體特性之影響]]
   - *關鍵成果*: 雙階 p-GaN + 超薄 UID-GaN 插入層阻絕 Mg 向外擴散；實現 E-mode ($V_{th}=+0.6\text{ V}$)；導通電阻降至 $2.5\ \Omega\cdot\text{mm}$；順向擊穿電壓 $11.6\text{ V}$；介面陷阱 $D_{it}$ 降低 70%，動態 $R_{on}$ 改善 1.8 倍。
5. **2026** | [[sources/2026_Chen_Composite_Dielectric_MIS_HEMT|陳思宏 - 複合式介電層對 AlGaN/GaN HEMT 閘極可靠度與崩潰機制之研究]]
   - *關鍵成果*: 原位氧電漿退火 GaON (2nm) + ALD $\text{Al}_2\text{O}_3$ (15nm) 雙層介電質；閘極關斷漏電壓低至 $10^{-8}\text{ mA/mm}$；順向擊穿達 $21.7\text{ V}$；常溫 10 年 TDDB 壽命達 $V_G = 12\text{ V}$；$BV_{off} \approx 1600\text{ V}$，$R_{on,sp} \approx 1.99\text{ m}\Omega\cdot\text{cm}^2$。
