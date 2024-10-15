這是一堂入門級的微學習課程，旨在探討大型語言模型 (LLM) 的定義和用途，並說明如何調整提示來提高 LLM 成效。此外，也會介紹多項 Google 工具，協助您自行開發生成式 AI 應用程式。

說明 LLM 的所有須知事項

Define Large Language Models(LLMs)
Describe LLM use case
Explain prompt tuning and describe Google's gen AI development tools

大型語言模型簡稱 LLM 是深度學習的分支 
如要進一步瞭解深度學習 請觀看課程影片 《Introduction to Generative AI》 
LLM 與生成式 AI 的部分領域重疊，二者都屬於深度學習的一環 

AI 另一個可能常聽到的 AI 領域 是生成式 AI，這是一種人工智慧 
能生成各種新內容 包括文字、圖片、音訊及合成資料 

什麼是大型語言模型？

![image](https://github.com/user-attachments/assets/f4880362-9e86-48c1-b43e-c6d925ad306b)

這是指一般用途大型語言模型 這是指一般用途大型語言模型 可預先訓練 並依據特定目的微調

「預先訓練」和「微調」又是什麼意思？

![image](https://github.com/user-attachments/assets/b62964de-d1d0-4119-9016-fb775e724e8c)

![image](https://github.com/user-attachments/assets/02b2df09-510d-4d40-a5f2-7bc59d38c2be)

以訓練狗狗為例 我們通常會訓練狗狗聽從基本的指令 例如坐下、過來、趴下、待在原地 這些指令通常就能滿足日常需求 還能讓狗狗成為聽話的寵物 好狗狗 
但如果需要特殊的服務犬 例如警犬、導盲犬或獵犬 就必須追加特別訓練，對嗎？

![image](https://github.com/user-attachments/assets/fd049a9f-d239-4254-8e98-2e4b0e5fbe3d)

![image](https://github.com/user-attachments/assets/40aed386-ae93-4760-ac63-ad80ebf9ed74)

類似的概念也適用於大型語言模型 這類模型的訓練是針對一般用途 
可以解決各領域常見的語言問題 例如文字分類、回答問題 文件摘要 以及生成文字 
這類模型還能用 規模較小的產業資料集進一步調整 這類模型還能用 規模較小的產業資料集進一步調整 
以解決零售業、金融業 和娛樂業等各領域特有的問題 以解決零售業、金融業 和娛樂業等各領域特有的問題 
有了初步認識後 接著來進一步拆解這個概念 深入瞭解 大型語言模型的三個主要特性

![image](https://github.com/user-attachments/assets/2e1c1796-3b16-4c71-b582-3035a5edcef3)

先介紹「大型」這個詞 這個詞有兩個意義 
第一個是指超大型的訓練資料集，有時可達 PB 規模 
第二個是指參數數量 在機器學習中 參數通常稱為超參數
基本上，參數是機器從模型訓練中 學到的記憶和知識 
參數決定了模型解決問題的能力 例如預測文字 因此我們使用「大型」這個詞 那「一般用途」呢？

「一般用途」是指 模型足以解決常見問題 形成此概念的原因有兩個 
第一個是無論執行何種工作 人類的語言模式都很相近 
第二個是資源限制 只有部分機構 能運用龐大資料集和極大量參數  
訓練這種大型語言模型 不如讓這些機構 建立基礎語言模型供他人使用？

![image](https://github.com/user-attachments/assets/c641d1d8-2392-454f-a41c-58eac625a3a0)

這帶出了最後兩個術語 「預先訓練」和「微調」 也就是使用大型資料集 
針對一般用途 預先訓練大型語言模型 
再用較小型的資料集微調 打造出具備特定功能的模型 
現在已確定 大型語言模型 LLM 的定義 現在已確定 大型語言模型 LLM 的定義 接著來說明

### LLM use cases LLM 的用途 

使用大型語言模型的好處顯而易見 使用大型語言模型的好處顯而易見
首先，透過單個模型就能處理多項工作  這些大型語言模型 在訓練中使用數 PB 的資料 並生成數十億個參數 

![image](https://github.com/user-attachments/assets/85bf9fba-b6c6-4e93-92f7-eb41e2a74784)

擅長處理各種工作 包括翻譯、完成語句、分類文字 回答問題等等 
其次，調整大型語言模型 來解決特定領域的問題時 其次，調整大型語言模型

來解決特定領域的問題時 需要的訓練資料不多 即使用少量的訓練資料 大型語言模型也能獲得不錯的成效 
換句話說 這類模型適用於 小樣本或甚至零樣本訓練情境 在機器學習中 

![image](https://github.com/user-attachments/assets/a3c48961-ae18-46a5-a936-ef9a5d486448)

![image](https://github.com/user-attachments/assets/11b6cf29-f191-49a5-832c-05e02b1c8493)

「小樣本」是指利用極少量資料訓練模型 
「零樣本」則表示模型可以辨識 先前未在訓練中明確學到的事物 
第三，隨著資料量和參數量增加 大型語言模型的成效也會持續增長 大型語言模型的成效也會持續增長

PaLM 這個例子 Google 在 2022 年 4 月推出 PaLM 這是 Pathways Language Model 的簡稱 
這個模型含有 5400億個參數 能在多種語言工作中 發揮頂尖成效 
PaLM 是 僅含有解碼器的稠密型 Transformer 模型 利用新的 Pathways 系統 

![image](https://github.com/user-attachments/assets/0fb55aba-bfaf-4499-9242-c8a37399f818)


![image](https://github.com/user-attachments/assets/f75e6a47-d489-4576-a7f7-338a5a503675)

讓 Google 能在多個TPU v4 Pod 中 有效率地訓練單一模型
Pathways 是新的 AI 架構 不僅能同時處理許多工作 快速接受新任務 
對現實世界的認知也更透徹 這套系統讓 PaLM 能自動化調度管理分散的加速器運算作業 
這套系統讓 PaLM

能自動化調度管理分散的加速器運算作業 不過我講太快了 先前提過 PaLM 是 Transformer 模型 

### Transformer model

![image](https://github.com/user-attachments/assets/0724ce54-6c6c-403f-a3df-157264c67068)

Transformer 模型 由編碼器和解碼器組成 
編碼器會將輸入序列編碼 然後傳給解碼器 解碼器會針對相關工作 學習如何解讀表徵 解碼器會針對相關工作

學習如何解讀表徵 從傳統程式設計、類神經網路到生成式模型 這個領域已有相當進展 
如果要辨識貓 傳統程式設計 通常必須透過硬式編碼來訂定規則 
傳統程式設計 通常必須透過硬式編碼來訂定規則 物種為動物、有四隻腳、兩隻耳朵 有毛、喜歡毛線球和貓薄荷 

![image](https://github.com/user-attachments/assets/d48b89c7-3933-42cb-bd00-a0fa31eb66ff)

隨著類神經網路的發展 我們只要提供貓和狗的圖片給類神經網路 然後詢問「這是貓嗎？」 
系統就能正確預測 值得一提的是 生成式技術崛起後 使用者就可以自行生成內容

像是文字、圖片、音訊、影片等 例如 PaLM (Pathways Language Model) 或 LaMDA (Language Model for Dialog Applications) 等模型 
都會從多種網際網路來源 擷取極大量的資料

![image](https://github.com/user-attachments/assets/beac32ee-2a3f-4eb8-92b3-5a2f4d4fbc06)

都會從多種網際網路來源 擷取極大量的資料 依此建構出基礎語言模型 使用者能透過輸入提示或口頭提問 直接向語言模型發問 當您詢問「什麼是貓」時 模型就會提供所有學過的貓類知識 現在來比較 使用預先訓練模型的 
LLM 開發作業 和傳統機器學習開發作業 首先，不是專家 也能進行 LLM 開發作業 不需訓練樣本

![image](https://github.com/user-attachments/assets/bcba50dc-cd01-4f9f-af53-06d435f0e751)

也不用自行訓練模型 您只需要思考如何設計提示 這是建立合適提示的過程 提示須簡單扼要且資訊充足 這是自然語言處理 (NLP) 中 很重要的一環 這是自然語言處理 (NLP) 中 很重要的一環 
如果是傳統機器學習開發作業 需要專業能力、訓練樣本、運算時間及硬體 相較於 LLM

![image](https://github.com/user-attachments/assets/0d3be061-956f-47e4-879e-c4b275396b35)

開發作業 需具備的條件更多 來看看文字生成用途的範例 來看看文字生成用途的範例 以實際瞭解剛剛的內容 
問題回答又稱 QA 是自然語言處理的子領域 負責自動回答 以自然語言提出的問題 負責自動回答 
以自然語言提出的問題 QA 系統通常會運用 大量文字和程式碼進行訓練 QA 系統通常會運用

![image](https://github.com/user-attachments/assets/f73c82f9-3612-4420-94d7-cd1bc2044a92)

![image](https://github.com/user-attachments/assets/17ea7b0b-b40c-467d-8065-f0860251b3d9)

大量文字和程式碼進行訓練 且能回答各類問題 包括事實性、定義性和觀點性問題 
包括事實性、定義性和觀點性問題 重點在於您必須擁有領域知識 才能開發這類問答模型 我用一個實際例子來說明 
如要開發 IT 客服 醫療照護或供應鏈的問答模型 必須具備領域知識

![image](https://github.com/user-attachments/assets/6b20dbff-9f4e-4655-9355-0c85238c8758)

但如果是生成式問答模型 就能直接根據背景資訊 生成任意文字 不須具備領域知識 讓我用更多例子 
來說明這項技術有多酷 來看看我問 Gemini 的三個問題

![image](https://github.com/user-attachments/assets/bf70f8d7-2533-4270-a34b-891bc6c2066e)

這是 Google AI 團隊開發的 大型語言模型聊天機器人 問題一：「今年銷售額是 $10 萬元營業費用是 $6 萬元 那麼淨利是多少？」 Gemini 會先說明淨利怎麼算 然後實際計算 接著，Gemini 會提供淨利的定義 
再來看另一個問題 「目前庫存有 6,000 件 新訂單需要 8,000 件 我需要增產多少件商品

![image](https://github.com/user-attachments/assets/6e3abca0-37df-40a0-81b7-4fc29f6bceee)

![image](https://github.com/user-attachments/assets/b3e0deba-b47e-4f3f-8df1-489a4a22517c)

才能完成訂單？」 同樣地，Gemini 會執行計算 並回答問題 最後一個例子 「我們在 10 個地理區域 裝設了 1,000 個感應器 每個區域平均裝設了幾個感應器？」 
Gemini 會提供問題的解法 並額外補充一些背景資訊 之所以能獲得每個問題所需的回覆 原因是什麼？

### Prompt design 提示設計

這都要歸功於 「提示設計」這個專業術語 「提示設計」和「提示工程」 這兩個自然語言處理概念密切相關 
兩者都需要建立提示 提示須簡單扼要且資訊充足 不過這兩者之間 還是有一些重要差異 

「提示設計」是指 找出合適提示的過程 根據使用者要求系統執行的特定工作 來建立相應提示 根據使用者要求系統執行的特定工作 來建立相應提示
例如，假設使用者要求系統 將文字從英文翻譯成法文 例如，假設使用者要求系統

將文字從英文翻譯成法文 那麼使用者應以英文撰寫提示 並指定要翻成法文 「提示工程」是指 為提升成效而建立相應提示的過程 過程中可能需要運用特定領域知識 提供理想輸出結果範例 或使用能在特定系統中 發揮良好成效的關鍵字 或使用能在特定系統中 發揮良好成效的關鍵字 「提示設計」較屬於一般概念 而「提示工程」則是較特殊的概念 「提示設計」不可或缺

![image](https://github.com/user-attachments/assets/a7b0d948-de4a-4db7-b8b2-a95a09eb5bbb)

高準確率或高效能時才需進行 大型語言模型分為三種
通用語言模型、指令調整模型 以及對話調整模型 

各模型的提示方法皆不同 
![image](https://github.com/user-attachments/assets/600c88aa-2cf8-48bb-b489-9a89342acd49)

![image](https://github.com/user-attachments/assets/a7defc1f-5f55-44f9-9106-e4299a805b71)

先來談談通用語言模型 這類模型會根據訓練資料中的語言 預測下一個字詞 這是通用語言模型 在「the cat sat on」這個例句中 下一個字詞應為「the」 「the」確實最有可能是下個字詞 這類模型 就好比搜尋系統的「自動完成」機制 


### 調整模型

![image](https://github.com/user-attachments/assets/9b9faa61-eda9-47bf-bfd9-0af4314a9f7d)

這類模型經過訓練後 能根據輸入內容中的指令預測回覆 
例如「統整 X 的文字內容」 「生成 X 風格的詩」「列出與 X 語意相似的關鍵字」 
在這個範例中 文字內容分類為中立、負面或正面 最後是對話調整模型 這類模型經過訓練後 能根據接下來的回覆來展開對話

![image](https://github.com/user-attachments/assets/0147f694-e7c8-466d-9770-d4d6583a0d76)

![image](https://github.com/user-attachments/assets/25d13814-35d5-43db-99e8-fa8a5a04093a)

![image](https://github.com/user-attachments/assets/ac5dccf3-40c4-4e5f-9a62-56c6f9e68b91)


對話調整模型是特殊的指令調整模型 對話調整模型是特殊的指令調整模型 使用者通常會以問句 向聊天機器人提出要求 使用者通常會以問句 向聊天機器人提出要求 這類模型適合用在 一來一往的長篇對話中 這類模型適合用在 一來一往的長篇對話中 且對自然問句的反應往往更好 且對自然問句的反應往往更好 我們觀察到模型的「關聯思考推論」能力 也就是模型輸出文字時 如果要它們先解釋背後的推理過程 它們更能提供正確的解答 來看個例題 「Roger

![image](https://github.com/user-attachments/assets/7dd1c6ec-e167-44b7-a15d-e9fe27339070)

![image](https://github.com/user-attachments/assets/caf98efc-0523-4f60-aa51-4db331d77f4e)

有五顆網球 他又買了兩筒網球 每筒裡有三顆網球 他現在共有多少顆網球？」 一開始這題並沒有獲得回應 因為模型難以直接取得正確的答案 

![image](https://github.com/user-attachments/assets/7f99d4cc-6c14-4ce3-80a6-4632204799ba)

但第二次提問時 輸出內容結尾 很可能就是正確的答案 不過，請特別留意 常常會有陷阱 泛用模型在實際應用上往往存在限制 不過，根據特定工作調整 LLM 能使其更可靠 

![image](https://github.com/user-attachments/assets/2529b7c6-2d2f-4fb7-857b-da58ad4e3364)

Vertex AI 針對特定工作提供基礎模型 現在來看看幾個實際例子

![image](https://github.com/user-attachments/assets/74721fe5-bc50-4ee9-9e1f-0d72377efad4)

瞭解如何調整模型 假設您需要收集 客戶對自家產品或服務的評價 假設您需要收集 客戶對自家產品或服務的評價 假設您需要收集 客戶對自家產品或服務的評價 您可以使用情緒分析工作模型 同樣概念也適用於視覺類工作 假設要執行車輛乘載人數分析 


我們也有專用的模型 在調整模型的過程中 您可以依據模型應執行的工作範例 自訂模型回應 

### Tuning 調整

![image](https://github.com/user-attachments/assets/09e45dd7-8912-4465-a10a-08d58a7f797a)

「調整」基本上就是用新資料訓練模型 以便應用於新領域 或一系列的自訂用途 例如，我們可以收集訓練資料

專為法律或醫藥領域調整模型 專為法律或醫藥領域調整模型 您還可以「微調」模型 加入自有資料集 並調整 LLM 的各項權重 
藉此進一步調整模型 這會需要大量訓練 並自行代管經過微調的模型 這是使用醫療照護資料 
訓練而成的醫療基礎模型 這是使用醫療照護資料 訓練而成的醫療基礎模型 
用途包括回答問題、分析影像 和找出類似病患等 多數情況下 微調模型的費用昂貴且不切實際 那麼，還有其他高效的調整方法嗎？

![image](https://github.com/user-attachments/assets/ff968833-3b3c-4f32-ae81-59cb6930a13e)

### PETM 

![image](https://github.com/user-attachments/assets/0b097d30-adc6-4d67-baaf-ac7ae303af03)

具參數運用效率的調整方法 (PETM) 指的是依據專屬自訂資料 調整大型語言模型 而無需複製模型 基礎模型不會有任何變化 取而代之的是調整少量附加層 在推論期間視需要交互替換 接著介紹另外三種方法 透過 Google Cloud 充分發揮 LLM 的功效

![image](https://github.com/user-attachments/assets/53d9c9f0-f3a2-4f86-b54c-afb8ba468be2)

首先是 Generative AI Studio 您可以在 Generative AI Studio 快速尋找及自訂生成式 AI 模型 您可以在 Generative AI Studio 快速尋找及自訂生成式

AI 模型 並用於自己的 Google Cloud 應用程式 Generative AI Studio 提供 各種簡單好上手的工具和資源 Generative AI Studio 提供 各種簡單好上手的工具和資源

![image](https://github.com/user-attachments/assets/d073950a-0c03-4078-b47b-c82980797613)

協助開發人員 建立及部署生成式 AI 模型 協助開發人員 建立及部署生成式 AI 模型 這些工具和資源 包含一系列預先訓練模型 模型微調工具 將模型部署至正式環境的工具 以及供開發人員 交流協作的社群論壇 以及供開發人員 交流協作的社群論壇

接著是 Vertex AI 這項工具非常適合 程式設計經驗不多的使用者 您可以使用 Vertex AI Search and Conversation 為客戶和員工打造 生成式 AI 搜尋與對話功能 為客戶和員工打造

![image](https://github.com/user-attachments/assets/c506434d-bcbe-42b1-b1af-90adb780d695)

數位助理、自訂搜尋引擎 知識庫、訓練應用程式等其他工具 最後是 PaLM API 這可讓您透過 Google 的大型語言模型和生成式 AI 工具 這可讓您透過 Google 的大型語言模型和生成式 AI 工具 進行測試和實驗

如要更輕鬆快速地設計原型 開發人員可整合 PaLM API 和 MakerSuite 這樣就能 透過圖形使用者介面存取 API 這樣就能 透過圖形使用者介面存取 API MakerSuite 提供多種工具 像是模型訓練工具、模型部署工具 以及模型監控工具 這些工具有什麼功用呢？

![image](https://github.com/user-attachments/assets/69a39d4e-b368-4b30-813e-4ade3f90047f)


這是個好問題 模型訓練工具 協助開發人員透過不同演算法 使用資料訓練機器學習模型 協助開發人員透過不同演算法 使用資料訓練機器學習模型 模型部署工具提供多種部署選項 方便開發人員 將機器學習模型部署到正式環境 方便開發人員 將機器學習模型部署到正式環境 模型監控工具則可讓開發人員 運用資訊主頁和各式各樣的指標 監控機器學習模型 在正式環境中的效能 監控機器學習模型 在正式環境中的效能 Gemini 是一種多模態 AI 模型 與傳統語言模型不同 不但可以解讀文字 還能分析圖片 瞭解音訊內容中的細節 甚至能解釋程式碼 因此

![image](https://github.com/user-attachments/assets/40261f68-4427-4124-a30b-fb3603a55b4d)

Gemini 可以執行 先前 AI 不能完成的複雜工作 因此 Gemini 可以執行 先前 AI 不能完成的複雜工作 Gemini 具備先進架構 因此適應力和擴充性都相當優異 適用於多種應用情境 Model Garden 會持續更新 加入新模型 看吧，在影片的一開始 我就說 我知道大型語言模型的相關資訊 現在您也知道了 感謝您觀看本課程 如要進一步瞭解如何使用 AI 請務必觀看我們的其他影片















