### 開始使用 Vertex AI Gemini API 和 Python SDK 
### Getting Started with the Vertex AI Gemini API and Python SDK

GSP1209

總覽
Gemini 是由 Google DeepMind 開發的一系列生成式 AI 模型，專為多模態用途而設計。
Gemini API 可讓您使用 Gemini Pro Vision 和 Gemini Pro 模型。在本研究室中，您將瞭解如何搭配使用 Vertex AI Gemini API 和 Vertex AI SDK for Python，
與 Gemini 1.0 Pro (gemini-1.0-pro) 模型和 Gemini 1.0 Pro Vision (gemini-1.0-pro-vision) 模型互動。


#### Vertex AI Gemini API

Vertex AI Gemini API 提供統一的 Gemini 模型互動介面。目前 Gemini API 有兩種可用模型：  
  
1. Gemini 1.0 Pro 模型 (gemini-1.0-pro)：專門處理自然語言工作、多輪文字和程式碼對話，也能生成程式碼。  
2. Gemini 1.0 Pro Vision 模型 (gemini-1.0-pro-vision)：支援多模態提示。您可以在提示要求中加入文字、圖片和影片，並取得文字或程式碼形式的回覆。  

與 Gemini API 互動的方法如下：

* 使用 Vertex AI Studio 快速測試並生成指令  
* 使用 cURL 指令  
* 使用 Vertex AI SDK
* 
本研究室聚焦於使用 Python 適用的 Vertex AI SDK 來呼叫 Vertex AI Gemini API。

詳情請參閱 Vertex AI 的生成式 AI 說明文件。
ref: https://cloud.google.com/vertex-ai/docs/generative-ai/learn/overview

#### 先備知識
開始本研究室之前，您應已熟悉以下概念：

* 對 Python 程式設計有基本的瞭解
* 具備有關 API 運作方式的一般知識
* 在 Vertex AI Workbench 中使用 Jupyter 筆記本執行 Python 程式碼


#### 目標
在本研究室中，您將瞭解如何執行下列工作：

* 安裝 Vertex AI SDK for Python  
* 使用 Gemini 1.0 Pro (gemini-1.0-pro) 模型生成文字  
* 使用 Gemini 1.0 Pro Vision (gemini-1.0-pro-vision) 多模態模型，從文字、圖片和影片組合中生成文字  


#### 工作 1：開啟 Vertex AI Workbench 中的筆記本
1. 前往 Google Cloud 控制台，依序點選「導覽選單」>「Vertex AI」>「Workbench」。  
2. 找出 Workbench instance name 執行個體，點選「Open JupyterLab」按鈕。
Workbench 執行個體的 JupyterLab 介面會在新瀏覽器分頁中開啟。

![image](https://github.com/user-attachments/assets/28fee38a-a9cf-4152-8e2f-975144e7b1c3)

![image](https://github.com/user-attachments/assets/a844889a-ba3c-45d6-b4de-84df7d18bfdb)

![image](https://github.com/user-attachments/assets/d902d42b-065c-4860-8037-1482e0b9edfb)

![image](https://github.com/user-attachments/assets/dfb4cdf7-bac5-4d87-bd0b-78a7eee8aaab)


#### 工作 2：設定筆記本
1. 按一下「notebook name」檔案。  
2. 執行筆記本的「Getting Started」和「Import libraries」部分。  
* 在「Project ID」部分使用「Project ID」，並在「Location」部分使用「Region」。

注意：您可以略過任何標有「Colab only」的筆記本儲存格。

![image](https://github.com/user-attachments/assets/061a2756-26a4-4200-93a7-e75ae03a27f4)


#### 工作 3：使用 Gemini 1.0 Pro 

Gemini 1.0 Pro (gemini-1.0-pro) 模型可處理自然語言工作、多輪文字和程式碼對話，也能生成程式碼。在這項工作中，請執行各個筆記本儲存格，瞭解如何透過文字提示使用 Gemini 1.0 Pro 模型生成文字。  

##### 使用文字提示來生成文字
請將文字提示傳送至模型。Gemini 1.0 Pro (gemini-1.0-pro) 模型採用逐句顯示機制，一旦生成片段即可著手處理，不必等模型提供完整回覆。

* 執行筆記本的「Generate text from text prompts」部分。

[] 使用文字提示來生成文字。
[] 顯示即時通訊記錄。

![image](https://github.com/user-attachments/assets/f49aac2d-d279-48e2-ad81-cbef90e88bd5)






#### 工作 4：使用 Gemini 1.0 Pro Vision 模型

Gemini 1.0 Pro Vision (gemini-1.0-pro-vision) 是支援多模態提示的多模態模型。您可以在提示要求中加入文字、圖片和影片，並取得文字或程式碼形式的回覆。在這項工作中，請執行各個筆記本儲存格，瞭解如何透過文字和圖片提示使用 Gemini 1.0 Pro Vision 模型生成文字，然後從影片檔案中生成文字。


#### 使用本機圖片和文字來生成文字
執行筆記本的「Generate text from local image and text」部分。

[] 驗證圖片。
[] 使用本機圖片和文字來生成文字。

#### 使用文字和圖片提示來生成文字

執行筆記本的「Generate text from text & image(s)」部分。

[] 使用文字和圖片來生成文字。

#### 合併多個圖片和文字提示來執行少量樣本提示

[] 執行少量樣本提示。

#### 從影片檔案中生成文字

執行筆記本的「Generate text from a video file」部分。

[] 從影片檔案中生成文字。

恭喜！
在本研究室中，您深入學習如何搭配使用 Vertex AI Gemini API 和 Vertex AI SDK for Python，與 Gemini 1.0 Pro (gemini-1.0-pro) 和 Gemini 1.0 Pro Vision (gemini-1.0-pro-vision) 這兩種模型互動。透過這些實作練習，您已充分瞭解 Vertex AI Gemini API 的功能，以及該 API 如何與 Python SDK 完美整合。









