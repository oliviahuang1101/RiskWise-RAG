# RiskWise AI｜風險管理與保險學智慧顧問

## 專案介紹
RiskWise AI 是一套結合檢索增強生成（Retrieval-Augmented Generation, RAG）技術的 AI 學習輔助系統，主要協助使用者理解風險管理與保險學相關概念。

本專案以課堂講義為知識來源，透過向量檢索找出與問題相關的教材，再由大型語言模型根據檢索結果產生回答，並提供教材引用，方便使用者查證。

## 主要功能
- **智慧問答：** 回答風險管理與保險學相關問題。
- **教材檢索：** 從 269 篇教材文件中搜尋相關內容。
- **概念解釋：** 提供專有名詞說明、概念比較及計算步驟。
- **來源引用：** 顯示參考教材的文件編號、標題與內容。
- **互動介面：** 使用 Gradio 建立網頁操作介面。

## 使用技術
- Python / Google Colab
- EmbeddingGemma 2
- FAISS 向量資料庫
- Groq API / GPT-OSS 120B
- Gradio
- GitHub

## 系統運作流程
1. 將保險學與風險管理教材整理為文字文件。
2. 使用 EmbeddingGemma 2 將文件轉換為向量。
3. 透過 FAISS 建立知識庫。
4. 使用者輸入問題後，檢索最相關的教材。
5. 將教材內容與問題提供給語言模型。
6. 產生繁體中文回答，並顯示參考來源。

## 知識庫
本儲存庫提供 `RiskWise_vector_embedding.zip`，內含 FAISS 索引、文件資料與設定檔，供 RAG 系統載入使用。

## 使用說明
開啟 RAG02 Google Colab，依序執行程式並設定自己的 Groq API Key，即可啟動 Gradio 介面進行問答。

[RAG02 Google Colab](https://colab.research.google.com/drive/1W9N_DxYPmS5gMlB3cBlqKtUoP5yNCdAx)

## 注意事項
本系統僅供課程學習與學術研究使用。AI 回答可能存在錯誤，重要資訊仍應以原始教材及正式資料為準。
