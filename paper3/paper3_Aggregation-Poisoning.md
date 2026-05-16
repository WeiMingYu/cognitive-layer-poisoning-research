# 技術預警：AI 聚合中心投毒與語義攔截路徑
## Technical Alert: Poisoning Vector in AI Aggregation Hubs

### 🛑 威脅背景 (Threat Context)

本文件定義了 **智能體攻擊鏈 (Agentic Kill Chain, AKC)** 中，關於「中間商與聚合中心」的投毒路徑。當開發者為了便利而使用第三方聚合工具（如 One API、New API 等）時，實則建立了一個具備「語義修改權」的單一崩潰點。

---

### 🧪 聚合中心投毒的技術路徑 (Attack Vectors)

1. **身份與權限偽造 (Identity Forgery)**
   * **機制**：聚合中心位處 Layer 1 (供應鏈層)，具備攔截 API 金鑰的權限。
   * **風險**：攻擊者可於背景以您的身份執行未授權的訓練、爬蟲任務，或將您的語義指紋轉賣。

2. **動態語義修改 (Dynamic Semantic Modification)**
   * **機制**：發生於 Layer 4 (語義層) 的中間人攻擊 (MITM)。
   * **風險**：中心可針對特定的「金融標的」或「決策指令」進行微調，在不改動 JSON 結構的情況下，導致 AI 代理人產生認知漂移，觸發錯誤決策。

3. **緩存毒化 (Cache Poisoning)**
   * **機制**：利用中心化的緩存機制進行集體操縱。
   * **風險**：將錯誤、過期或經過修飾的資訊餵給不同使用者，引發群體性的認知偏差與市場操縱行為。

---

### 🛡️ 給白帽研究員的採證清單 (Forensic Checklist)

建議研究人員針對聚合中心進行以下實測，以驗證語義完整性：

* **一致性對比 (Consistency Audit)**
    * 同時串接「原廠 API」與「聚合中心 API」。
    * 對比同一問題在兩者回傳結果中的 Token 分佈、數值精準度與語義偏移率。

* **延遲與流量分析 (Traffic Latency Analysis)**
    * 監控當請求包含敏感金融詞彙時的處理延遲。
    * 異常的高延遲通常代表中心正在執行動態語義過濾或攔截邏輯。

* **注入攻擊測試 (Injection Stress Test)**
    * 使用研究中的 **Layer 3 (Token 層)** 攻擊向量，如注音、文言文、繁簡混合編碼。
    * 測試過濾器是否崩潰，或是否會將混淆編碼誤轉譯為攻擊者預設的指令。

---

### ⚠️ 研究聲明 (Disclaimer)

本清單僅供防禦性研究與學術探討。在語義空間的「完美犯罪」成為現實前，我們必須先建立透明的採證標準。

**Author**: WeiMing Yu  
**Research Project**: Cognitive Layer Poisoning via Multi-Agent Interaction (CLPMAI)
