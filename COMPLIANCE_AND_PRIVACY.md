# ⚖️ Corporate Compliance, Privacy & Regulatory Applicability Declaration
# 企業合規、私隱保護與法規適用性聲明

**Document Classification:** Public / Enterprise Governance  
**Applicable System:** Enterprise Governance & Workflow Engine (Demo)  

---

## 1. System Classification & AI Out-of-Scope Declaration (系統分類與 AI 豁免聲明)

**[EN]**  
To ensure strict compliance with global digital governance standards, a formal assessment has been conducted regarding the nature of this system. This project is classified as a **Deterministic Rule-Based Workflow and Robotic Process Automation (RPA) Engine**. It operates strictly on pre-defined logic (e.g., condition gates, approvals) and does **NOT** utilize Machine Learning (ML), Deep Learning, or Generative AI models. Consequently, AI-specific regulations are formally evaluated as **Out of Scope**.

**[TC]**  
為確保嚴格遵守全球數碼治理標準，本專案已完成正式的系統性質評估。本系統被歸類為**「確定性規則工作流與自動化（RPA）引擎」**。系統嚴格依賴預設邏輯（如條件閘道、審批流）運作，**並未**使用任何機器學習（ML）、深度學習或生成式 AI 模型。因此，針對人工智能之特定法規，於本系統中正式列為**不適用（Out of Scope）**。

---

## 2. Regulatory Applicability Matrix (法規適用性評估矩陣)

| Regulation / Standard (法規與標準) | Applicability (適用性) | Rationale & Implementation (評估理據與落實情況) |
| :--- | :--- | :--- |
| **Hong Kong PDPO (Cap. 486)**<br>香港《個人資料(私隱)條例》 | **Highly Applicable**<br>高度適用 | **Compliant.** Strictly adheres to Data Protection Principles (DPPs). Only essential personal data for declarations is collected, securely stored, and protected against unauthorized access. (全面落實保障資料原則，僅收集申報所需之必要資料，並嚴防未經授權之存取。) |
| **EU GDPR**<br>歐盟《通用數據保障條例》 | **Applicable**<br>適用 | **Privacy by Design.** Implements role-based access control (RBAC) and audit trails. Data minimization is enforced at the collection source. (由設計展現私隱。實施角色權限控制與審計追蹤，於收集源頭落實資料極小化。) |
| **ISO/IEC 27001 & 27701**<br>資訊安全與私隱資訊管理 | **Highly Applicable**<br>高度適用 | **Compliant.** Source code is decoupled from sensitive enterprise data. Immutable audit logs (timestamps) are generated for all approval actions to ensure data integrity. (源碼與企業敏感數據解耦。所有審批動作均生成不可篡改之時間戳記審計日誌，確保資料完整性。) |
| **EU AI Act**<br>歐盟《人工智能法案》 | **Out of Scope**<br>不適用 | Not an AI system under Article 3(1). Does not use statistical ML or generative models, thus exempt from Annex III high-risk AI obligations. (本系統非屬該法案定義之 AI 系統，免除高風險 AI 系統之合規義務。) |
| **ISO/IEC 42001:2023 (AIMS)**<br>人工智能管理體系 | **Out of Scope**<br>不適用 | System employs deterministic Microsoft 365 / Low-code workflows rather than adaptive AI algorithms. (採用確定性自動化工作流，無自適應 AI 演算法，故無需建立 AIMS。) |
| **CAC Generative AI Measures**<br>中國網信辦《生成式人工智能服務管理暫行辦法》 | **Out of Scope**<br>不適用 | No generative capabilities (text/image/video generation) are present. (系統不具備生成式內容能力，不受該暫行辦法管轄。) |

---

## 3. Data Privacy & Security Policy (數據私隱與資訊安全政策)

### 3.1 Data Minimization & Retention (資料極小化與留存)
**[EN]** The system collects strictly what is necessary for internal auditing (e.g., employee ID, declaration details, timestamps). Data is retained solely on the enterprise's secure cloud tenant (e.g., SharePoint) and is governed by the organization's official data retention schedule.  
**[TC]** 系統僅收集內部審計絕對必要之數據（如員工編號、申報詳情、時間戳記）。數據僅留存於企業安全的雲端租戶（如 SharePoint）內，並受機構官方資料保留期限政策管轄。

### 3.2 Auditability & Closed-Loop Governance (可審計性與閉環管治)
**[EN]** All actions within the system (submissions, approvals, rejections, acknowledgments) generate immutable digital footprints. The system is designed to provide complete traceability for internal and external auditors (e.g., Anti-Corruption compliance).  
**[TC]** 系統內所有操作（提交、審批、退回、知悉確認）均會生成不可篡改之數位足跡。系統架構旨在為內部及外部審計（如防貪合規審查）提供 100% 的可追溯性。

---

## 4. Legal Disclaimer (法律免責聲明)

**[EN]**  
This system operates as a workflow automation and governance support tool. It does not replace professional legal, HR, or compliance advice. The enterprise and the developers assume no liability for administrative errors, organizational policy breaches, or technical interruptions resulting from the use of this system.

**[TC]**  
本系統僅作為工作流自動化與管治輔助工具，絕不取代專業法律、人力資源或合規意見。企業及開發者對因使用本系統而引致之行政錯誤、組織政策違規或技術中斷，概不承擔任何法律責任。
