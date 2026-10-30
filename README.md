# 🏗️ 企業展示員工手冊智能查詢系統 (EnterpriseDemo-StaffHandbookRAG)

An AI-powered Enterprise RAG Assistant for Corporate Staff Handbooks and HR Policies.  
專為現代化企業打造之企業級 HR 政策與《員工手冊》智能對答系統（展示版本）。

---

## 🌐 項目簡介 / System Overview

**EnterpriseDemo-StaffHandbookRAG** 是一個基於檢索增強生成（RAG, Retrieval-Augmented Generation）技術的智能查詢系統。系統結合了語意檢索與關鍵字精確比對，協助企業員工快速定位《月薪員工手冊》及最新人力資源政策通告，同時確保企業數據安全與政策時效性。

**EnterpriseDemo-StaffHandbookRAG** is an enterprise AI assistant designed for corporate employees to query company staff handbooks and updated HR policies. Built on Retrieval-Augmented Generation (RAG) technology, it combines semantic search and exact keyword matching to deliver accurate, traceable, and up-to-date compliance guidance while maintaining strict privacy standards.

---

## ✨ 核心特色 / Key Features

- **雙引擎混合檢索 (Ensemble Hybrid Retrieval)**
  - 結合 **FAISS (向量語意搜尋)** 與 **BM25 (關鍵字比對)**，兼顧口語化提問與精確條文編號（如 Demo-Form 表格）。
  - Integrates **FAISS (Vector Semantic Search)** and **BM25 (Keyword Matching)** via Reciprocal Rank Fusion (RRF) for optimal recall precision.
- **最新政策動態覆蓋 (Policy Overriding & Lifecycle Mapping)**
  - 支援動態政策摘要（如 2026 人面識別考勤、薪酬架構優化、培訓資助），自動提示最新通告並置頂，防止舊版條文誤導。
  - Dynamically overrides legacy handbook clauses with latest policy addendums (e.g., 2026 Facial Recognition Attendance, Compensation Structure), ensuring users receive the most current instructions.
- **確定性章節路由與雜訊過濾 (Chapter Routing & Noise Filtering)**
  - 內建確定性索引與正則表達式，精確鎖定目標章節（如培訓資助強制聚焦第九章），並自動剔除頁首頁尾雜訊 Chunk。
  - Built-in rule-based routing and regex pattern matching to bind topics to correct chapters and sanitize text chunk noise.
- **企業合規與導航 (Enterprise Governance Guidance)**
  - 提供內部共享資料夾 (`Z:\HR-Public Folder\Policies`) 的完整指引，確保權威條文可追溯。
  - Directs users to official internal drive paths for full regulatory documentation and forms.

---

## 🔒 數據安全與 ISO 合規 / Security & ISO Compliance

本系統在架構設計上嚴格落實 **AI 治理與風險管控 (AI Governance & Risk Management)**，符合多項國際標準精神：

- **ISO/IEC 42001 (Artificial Intelligence Management System)**
  - **Zero Data Retention**: 純本地 Session 暫存與記憶體運算，關閉網頁或清除對話時所有數據徹底銷毀，不做模型訓練。
  - **Traceability & Transparency**: 檢索結果明確標註來源檔案名稱、章節與實體頁碼（例如：第 15 頁），達成 100% 輸出可追溯。
- **ISO/IEC 27001 (Information Security Management System)**
  - **Data-Code Separation**: 商業敏感資訊（如薪酬細節）進行脫敏化處理，並解耦至外部配置，確保程式碼倉庫不洩漏企業機密。
  - **Secure Disposal**: 採用 `try...finally` 安全例外處理機制，檔案解析後自動清空臨時文件。

---

## 🛠️ 技術棧 / Tech Stack

- **Frontend / UI**: Streamlit 1.32.0
- **RAG Framework**: LangChain
- **Vector Index / Search**: FAISS (`faiss-cpu`)
- **Keyword Search**: BM25 (`rank_bm25`)
- **Embedding Model**: `sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2`
- **PDF Parser**: `pypdf`

---

## 📁 專案結構 / Project Structure

```text
EnterpriseDemo-StaffHandbookRAG/
├── app.py                  # Streamlit 主程式 (Main Application)
├── policy_overrides.json   # 最新政策動態配置 (Dynamic Policy Overrides Config)
├── requirements.txt        # 依賴套件清單 (Python Dependencies)
├── README.md               # 系統說明文件 (Project Documentation)
├── index.html              # GitHub Pages 靜態展示頁 (Landing Page)
└── COMPLIANCE_AND_PRIVACY.md # 企業管治與法規聲明 (Governance Declaration)

```
