**介紹擴散模型 Introduction to Image Generation**

這一系列的模型 近期在圖像生成領域展現亮眼潛力 近期在圖像生成領域展現亮眼潛力 雖然許多做法已導入圖像生成 但長期下來 我們發現有幾個系列模型 較具發展潛力  

# Image Generation Model Families (圖像生成模型家族)

This image outlines three main families of image generation models:

## Variational Autoencoders (VAEs) (變分自動編碼器)

這個模型會將圖像編碼成壓縮後大小 再解碼將圖像恢復為原始大小 同時學習資料本身的分布情形 生成對抗網路讓兩個類神經網路對抗    

* **Description:** Encode images to a compressed size, then decode them back to the original size while learning the distribution of the data.
* **描述：** 將圖像編碼為壓縮大小，然後解碼回原始大小，同時學習數據的分布。

## Generative Adversarial Models (GANs) (生成對抗網路)
* **Description:** Pit two neural networks against each other.
* **描述：** 讓兩個神經網路相互對抗。

另一個類神經網路「鑑別器」 則預測圖像的真實性 鑑別器分辨圖像真假的能力 會隨著時間提高 而生成器會越來越擅長 製作出幾可亂真的圖像 
自我迴歸模型是將圖像 視為像素序列來處理 自我迴歸模型現在的做法 是參考 LLM (大型語言模型)  

### Autoregressive Models (自迴歸模型)
* **Description:** Generate images by treating an image as a sequence of pixels.
* **描述：** 透過將圖像視為像素序列來生成圖像。

### 處理文字的方式

擴散模型的靈感是來自物理學 具體來說是熱力學 
這類圖像生成模型 在 2015 年問世 但這個概念花了好幾年 才真正廣為流傳

![image](https://github.com/user-attachments/assets/b172e314-2c94-4e7d-9028-9e9966115304)

擴散模型在各種不同用途 皆能派上用場

1. 無條件式擴散模型

也就是沒有額外輸入 內容或指示的模型 可用特定物體的圖像加以訓練 來生成該物體的新圖像 例如臉部

2. 條件式擴散模型

條件式擴散模型 則具備將文字轉圖像的能力 也就是根據文字提示生成圖像 並進行圖像編輯 也就是根據文字提示自訂圖像 

![image](https://github.com/user-attachments/assets/c923a69e-1751-4c1e-bbb4-b75c72082cda)

![image](https://github.com/user-attachments/assets/f8bc2da3-b93e-4f8d-8e8f-6441b570655b)


![image](https://github.com/user-attachments/assets/6cd3eb52-299f-47e9-b470-e4d57e8a5be4)

![image](https://github.com/user-attachments/assets/cc125b2d-f3d7-465a-ae77-acfb0c599795)

![image](https://github.com/user-attachments/assets/8d110136-4bed-442b-91b9-a95faf81912d)

這裡我們先取 畫面左邊的單一圖像 開始正向擴散程序 從初始圖像 X0 到 帶有一點雜訊的初始圖像 X1 接著不斷執行這個步驟 重複疊加更多雜訊至圖像 我們將這個分布稱為 q 這只取決於上一個步驟 接著不斷執行這個步驟 反覆加入更多雜訊 當疊加數量達到 T 時 應該就能獲得純雜訊 最初相關的研究報告 採用 T = 1,000 而現在我們將反向操作 如何將充滿雜訊的圖像 XT 轉變成雜訊稍微較少的圖像 XT-1？

![image](https://github.com/user-attachments/assets/43b19e33-2505-43d3-8a1f-7d8c36aa647d)

中取樣 來製作雜訊圖像 我們訓練除雜訊模型來預測雜訊 這個模型的訓練目的是 盡可能減少預測雜訊和 疊加至圖像的真實雜訊 兩者之間的差異 也就是說，這個模型可以 從真實圖像中移除雜訊 如要生成圖像 可以從純雜訊著手 並將其傳送至除雜訊模型 我們能將預測的雜訊 從初始雜訊中排除 如果我們不斷執行這個程序 最終模型就會生成圖像 也就是說 模型能透過這個過程

![image](https://github.com/user-attachments/assets/3579861f-f40c-4f7e-95b7-233651043fa8)

![image](https://github.com/user-attachments/assets/951ed30f-3a1f-437c-88b7-8bc7c06cf5d1)

瞭解自己看到的圖像資料 並從學習分布中取樣 以製作出全新圖像 我相信大家都知道 過去幾年來 這個領域已取得許多進展 在使用 Vertex AI 生成圖像方面 也有許多令人期待的全新技術 是以擴散模型為基礎 生成圖像變得更快速 您也能進一步控管圖像生成流程 此外，我們還發現結合擴散模型 和大型語言模型的強大能力會帶來驚人成效 模型能根據背景資訊 生成令人驚豔的逼真圖像
05:19
模型能根據背景資訊 生成令人驚豔的逼真圖像 最佳例子就是 Google 研究的圖像 雖然這個模型 和之前介紹的模型相對複雜了些 但核心概念其實就是由大型語言模型 和幾個擴散型模型所組成 這是我們引以為傲的成果 很榮幸看到這項技術 成為 Vertex AI 的企業級產品 感謝您觀看本影片 如想進一步瞭解類似主題 歡迎觀看我們的其他影片


Q&A

**1. 哪個模型系列的命名靈感來自物理學和熱力學？**
*擴散模型。
變分自動編碼器。
自我迴歸模型。
生成對抗網路。

**What is the name of the model family that draws inspiration from physics and thermodynamics?**
**Diffusion models**
Variational autoencoders
Generative adversarial networks
Autoregressive models


**2. 在處理過程中，哪個模型會學著從圖像中移除雜訊？**
X正向擴散
取樣
生成對抗網路 (GAN)
*反向擴散

**Which process involves a model learning to remove noise from images?**
Forward diffusion
Sampling
GANs
**Reverse diffusion**


**3. 擴散模型面臨哪些挑戰？**
訓練模型的運算成本可能相當高。
這種模型可能會產生不真實的圖像。
這種模型可能難以控制。
*以上各項。

**What are some challenges of diffusion models?**
They can generate images that are not realistic.
They can be difficult to control.
**All of the challenges listed are correct.**
They can be computationally expensive to train.




**5. 什麼是正向擴散過程？**  
X從有雜訊的圖像開始疊代移除雜訊。
從有雜訊的圖像開始隨機移除雜訊。
從未經處理的圖像開始隨機增加雜訊。
從未經處理的圖像開始疊代增加雜訊。

**What is the process of forward diffusion?**
Start with a noisy image and remove noise randomly
**Start with a clean image and add noise iteratively**
Start with a clean image and add noise randomly
Start with a noisy image and remove noise iteratively




7. 擴散模型的目標是什麼？  
將圖像做為向量序列來產生圖像。
X透過編碼壓縮圖像大小，再解碼將圖像恢復為原始大小。
根據資料點在潛在空間的擴散方式建立模型，學習資料集的潛在結構。
讓兩個類神經網路對抗。

**What is the goal of diffusion models?**
To generate images by treating an image as a sequence of vectors
**To learn the latent structure of a dataset by modeling the way in which data points diffuse through the latent space**
To pit two neural networks against each other
To encode images to a compressed size, then decode back to the original size

