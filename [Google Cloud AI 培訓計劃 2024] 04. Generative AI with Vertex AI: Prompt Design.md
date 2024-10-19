Generative AI with Vertex AI: Prompt Design



### GSP1154
總覽
設定和需求
工作 1：透過 Gemini Freeform 分析圖片
工作 2：探索任意形式功能
工作 3：運用任意形式和結構化模式來設計提示
工作 4：生成對話


### 總覽
Vertex AI 是全方位的機器學習開發平台，提供預測式和生成式 AI 功能，方便您訓練、評估及部署預測機器學習模型來預測趨勢。此外，您可以利用平台探索、調整及提供生成式 AI 模型來產生內容。

有了 Vertex AI Studio，您就能快速測試及自訂生成式 AI 模型，並用於應用程式。這個平台提供各種工具和資源，包括使用者介面 (UI) 和程式碼範例，即使您沒有機器學習相關背景，也能輕鬆開始使用生成式 AI。

本實作實驗室會逐步說明 Vertex AI Studio，協助您發揮先進生成式 AI 模型的潛在價值。您將探索 Gemini Freeform，直接在 Google Cloud 控制台用於分析圖片、設計提示及生成對話。透過直覺的使用者介面即可開始使用，不需要 API 或 Python SDK。

Vertex AI Studio: https://cloud.google.com/generative-ai-studio


### 目標
在本實驗室中，您會執行下列工作：  

*透過 Gemini Freeform 分析圖片。  
*探索任意形式功能。  
*運用任意形式和結構化模式來設計提示。  
*生成對話。  

### Task 1. Analyze images with Gemini in Freeform mode

### 啟用 Vertex AI API
在 Google Cloud 控制台頂端的搜尋列中輸入 Vertex AI API。  
點選「Marketplace 與 API」下方的 Vertex AI API 搜尋結果。  
點選「ENABLE」。  

![image](https://github.com/user-attachments/assets/986923ad-ee8f-43a4-9005-b96a9b2ca246)

![image](https://github.com/user-attachments/assets/c0ea66a8-210d-4744-8958-74c701164ede)

![image](https://github.com/user-attachments/assets/a929f7b4-bead-4ecb-968c-a9932b29947f)


1. In the Google Cloud console, from the Navigation menu (Navigation menu), select Vertex AI > Vertex AI Studio > Overview.  
1. 前往 Google Cloud 控制台，依序點選「導覽選單」 導覽選單 >「人工智慧」>「Vertex AI」>「Vertex AI Studio」>「總覽」。 

![image](https://github.com/user-attachments/assets/ddda02df-a5eb-4b7d-bfb3-ce2a5b380a77)


您會看到四項功能：「任意形式」、「聊天」、「視覺」及「語音」，本實驗室著重在前兩項。

2. 如要透過 Gemini 生成內容，請點選「開啟任意形式文字」。

![image](https://github.com/user-attachments/assets/d2aa1d5d-52d2-4321-a6de-bee22ff145a8)

請注意，UI 分為三大區塊：  
提示 (位於頂端)：您可以在這裡建立運用任意形式功能的工作。  
設定 (位於右方)：您可以在這裡選取模型、設定參數並取得相應的程式碼。  
回覆 (位於底部)：這裡會顯示工作結果。  
  
Prompt (located in the center): Here, you can create a prompt that utilizes multimodal capabilities.  
Configuration (located on the right): This section allows you to select models, configure parameters, and obtain the corresponding code.  
Response (located at the bottom): This section displays the results of your prompt.  

![image](https://github.com/user-attachments/assets/5ffc5e45-ddb6-4399-b1e9-65a555224d86)

3. On the top left, click Untitled Prompt and rename your prompt as Image Analysis.
   將提示命名為圖片分析。

![image](https://github.com/user-attachments/assets/ae208917-f463-4c95-ab28-e2a07be0085f)

4. In the Configuration section on the top right, click on the Model dropdown then select the gemini-1.5-pro model.

5. Download the sample image. Right-click the timetable image and then save it to your desktop.
   下載範例圖片。在時刻表圖片上按一下滑鼠右鍵，然後存到電腦。

7. On the top right of the Prompt section, click Insert media > Upload. Upload the timetable image you downloaded. The media can be in the form of an image, video, text, or audio file.
   生成圖片標題。依序點選右上方的「插入媒體」>「上傳」，然後上傳時刻表圖片。這類媒體可以是圖片或影片。

![image](https://github.com/user-attachments/assets/d0d39a2f-d109-4178-aebd-af06dabe10bc)

![image](https://github.com/user-attachments/assets/d3db6481-d37c-4b66-83d3-7d78231df8d7)

![image](https://github.com/user-attachments/assets/cd6315d9-4e9d-431e-be45-6ffb3f4fed2d)

```
Title the image.
```

8. The image will be displayed inside of the Prompt section. Copy the following text and paste it under the image and click on the Submit button on the bottom right of the Prompt section.
   說明圖片。將之前的提示換成下列文字，然後點選「SUBMIT」(提交)。  

```
Describe the image in detail.
```

![image](https://github.com/user-attachments/assets/8893c360-0cc8-40f3-a601-10caec61ec48)


9. Tune the parameter. In the Configuration section, adjust the temperature by scrolling from left (0) to right (2). Resubmit the prompt to observe any changes in the outcome compared to the previous result.  
   調整參數。從左 (0) 捲至右 (1)，調整隨機性參數。重新提交提示，與先前結果相比，觀察結果是否有任何變化。  

注意：隨機性參數會決定選取詞元的隨機程度。如果您想藉由提示生成正確或適當的回覆，建議調低隨機性參數。另一方面，如果隨機性參數較高，則可能產生較多元或預料之外的結果。如果隨機性參數為 0，系統一律會選取可能性最高的詞元。

10. 從圖片擷取文字。將之前的提示換成下列文字：  
    
```
Read the text in the image.
```

接著，如要以清單呈現輸出內容，請將之前的提示換成下列文字：  

```
Parse the time and city in this image into a list with two columns: time and city.
```

![image](https://github.com/user-attachments/assets/84d5242f-a4de-4039-8269-c47b9147051f)


11. 分析圖片中的資訊。將之前的提示換成下列文字：

```
Calculate the percentage of the flights to different continents.
```

結果是否符合預期？強烈建議對不同的工作試試別的提示，或是用不同的隨機性參數設定進行測試，觀察結果有何變化。

12. 儲存提示。設計好提示後，請點選「儲存」。如果出現選取區域的提示，請選取下拉式選單中的 us-central1，然後點選「儲存」來確認設定。如要找出先前儲存的提示，請前往「已儲存的提示」。  
13. Once you finish the prompt design, save the prompt by clicking Save on the top right of the Configuration section. For the region, select us-central1 from the dropdown and then confirm by clicking Save.  
    To find your saved prompts, on the left-hand navigation menu, navigate to Prompt Management.
    
注意：選取「儲存」後，請先稍候幾秒鐘，等待提示正確儲存完畢，再進行實驗室的後續步驟。  

![image](https://github.com/user-attachments/assets/b3e29a30-7d40-4eba-a281-ad014878784f)


![image](https://github.com/user-attachments/assets/606cd44c-9da4-4d3f-8de6-b4f418919f22)


![image](https://github.com/user-attachments/assets/27a40ca9-d649-423d-95f6-bcb6bec16666)


### Task 2. Explore multimodal capabilities 工作 2：探索任意形式功能

In addition to images, text, and audio, Gemini is capable of accepting videos as inputs and generating text as an output.  
  
除了圖片和文字之外，Gemini Freeform 也支援輸入影片並生成文字。  

1. 依序前往「Cloud Storage」>「值區」，複製 Cloud Storage bucket 名稱，這稍後會用到。
   Navigate to Cloud Storage > Buckets and copy the name of your Cloud Storage bucket and save it to use in the further step.

![image](https://github.com/user-attachments/assets/af3cffac-2728-4e77-b82a-b8fb426655a6)


2. 點選「啟用 Cloud Shell」，然後執行下列指令，將影片樣本 gs://spls/gsp154/video/train.mp4 (預覽) 複製到 Cloud Storage bucket。
   Click Activate Cloud Shell Activate Cloud Shell icon at the top of the Google Cloud console.

![image](https://github.com/user-attachments/assets/5f3bc78a-1e4e-41b2-8868-695721a47108)

注意：請務必將 <Your-Cloud-Storage-Bucket> 換成剛剛複製的 bucket 名稱。

![image](https://github.com/user-attachments/assets/be182e23-4e85-415d-a350-9da97e24537b)

3. 再次前往「Vertex AI」>「Vertex AI Studio」>「總覽」。
   In your Cloud Shell terminal, run the command below to copy the sample video gs://spls/gsp154/video/train.mp4 (preview) to your Cloud Storage bucket. Replace <Your-Cloud-Storage-Bucket> with the bucket name you copied earlier.

![image](https://github.com/user-attachments/assets/5bc2d23d-a3bc-4b0f-91d1-785d64931fd3)

4. 如要透過 Gemini 生成內容，請點選「開啟任意形式文字」。 Under Generate with Gemini, click Open Freeform.

5. 依序點選「插入媒體」>「從 Cloud Storage 匯入」。Click Inset Media > Import from Cloud Storage.

![image](https://github.com/user-attachments/assets/4496be75-dd2f-486b-93fe-d6199e6749c7)

6. 依序點按 bucket 名稱和影片樣本 (即 train.mp4)，然後按一下「選取」。 Click on your bucket name and then click on the sample video i.e., train.mp4 and click Select.

![image](https://github.com/user-attachments/assets/e49f181c-6465-4ecf-bc36-c68cdd381d03)

  
7. 插入自己的提示，生成任意影片資訊。Generate information about the video by inserting the following prompt and clicking the Submit button.

```
Title the video.
```

![image](https://github.com/user-attachments/assets/31dc4469-bf5c-480f-93af-5f1e3e6db3d7)

![image](https://github.com/user-attachments/assets/0bfb739f-0031-4eae-ba80-95040c786ff5)

Freeform mode offers many capabilities such as writing stories from images, analyzing videos, and generating multimedia ads. Explore more freeform use cases by clicking Prompt gallery. Check out more information about design multimodal prompts.

https://cloud.google.com/vertex-ai/docs/generative-ai/multimodal/design-multimodal-prompts

### 工作 3：運用任意形式和結構化模式來設計提示 Task 3. Design text prompts

In this section, you will explore designing text prompts in Vertex AI Studio. You will explore zero-shot, one-shot, and few-shot prompting.

1. 回到「Vertex AI Studio」>「任意形式」頁面。

點選「開啟任意形式文字」按鈕，如下圖所示。實際 UI 可能會與螢幕截圖稍有不同。

#### 提示設計
您可以視需求輸入文字，例如向模型提問，模型就會根據提示結構回覆。找出及設計最適當的輸入文字 (提示)，讓模型提供所需的回覆，這個過程稱為提示設計。

關於設計提示的最佳方式，目前仍沒有定論。您可以透過 3 種方法讓模型生成所需的回覆：

零樣本提示Zero-shot prompting：僅給予 LLM 工作說明的提示，而不提供其他資料。舉例來說，如果要 LLM 回答問題，就直接輸入「什麼是提示設計？」這樣的提示。

單樣本提示One-shot prompting：針對要求 LLM 執行的工作給予一個工作樣本。舉例來說，如果要 LLM 寫詩，您可以先提供一段詩詞樣本。

少量樣本提示Few-shot prompting：針對要求 LLM 執行的工作給予少量工作範例。舉例來說，如果要 LLM 撰寫新聞文章，您可以先提供幾篇文章。

任意形式：您可以輕鬆設計提示，不需要額外提供樣本，適合數量不多的實驗性提示。這種形式可用來探索零樣本提示，此外，您還可以使用範本加入情境和多個樣本，這對之後會提到的單樣本和少量樣本提示方法尤為實用。

任意形式 Parameters
Temperature and Token limit are two important parameters that you can adjust to influence the model's response.

Temperature controls the randomness in token selection. A lower temperature is good when you expect a true or correct response. A temperature of 0 means the highest probability token is always selected. A higher temperature can lead to diverse, unexpected, or potentially biased results. The gemini-1.5-pro model has a temperature range of 0 - 2 and a default of 1.
Output token limit determines the maximum amount of text output from one prompt. A token is approximately four characters.


### Zero-shot prompting

Try zero-shot prompting in Free-form mode.

1. Navigate back to the Vertex AI Studio > Overview page and click Open Freeform.

2. 將下列文字複製到提示輸入欄位。保留目前預設的模型設定：Gemini 1.5 Pro。 On the top right under Model, select the gemini-1.5-pro model.

![image](https://github.com/user-attachments/assets/8fa7e844-97b5-4810-8b38-eb9f18cb9347)

Note: The model name and version may change with the release of new models.  
注意：發布新模型時，模型名稱可能會變更。  

3. Copy the following over to the prompt input field:

4. Click on the Submit button.

您可以試試下列幾個做法，瞭解提示的運作原理。

將 Output token limit 參數調整為 1，然後點按「提交」按鈕
將 Output token limit 參數調整為 1024，然後點按「提交」按鈕
將 Temperature 參數調整為 0.5，然後點按「提交」 按鈕
將「Temperature」調整為 1.0，點選「提交」按鈕

Here are some exploratory exercises to explore.

Adjust the Output Token limit parameter to 1024 and click the SUBMIT button.
Adjust the Temperature parameter to 0.5 and click the SUBMIT button.
Adjust the Temperature parameter to 2.0 and click the SUBMIT button.

### 設計及管理提示 One-shot prompting

您可以更有條理地設計提示，在相應輸入欄位中提供情境和樣本，瞭解單樣本和少量樣本提示的運作方式。

You can design prompts in more organized ways. You can provide Context and Examples in their respective input fields. One-shot prompting is a method where the model is given a single example of the task that it is being asked to perform. In this section, you will ask the model to complete a sentence.

在本節中，您將要求模型完成一個句子。

1. 返回「文字提示」視窗。 Start by removing any text from the Prompt box.   

2. 點選頁面頂端的「新增樣本」。 Inside of the Prompt box, click Add examples. This will open a new window where you can add examples for the prompt.

![image](https://github.com/user-attachments/assets/8a0149eb-7a13-462b-9897-4acb56d9b3f9)

![image](https://github.com/user-attachments/assets/7061354d-45f8-4352-addc-a309dc8f8966)

將下列文字新增至「INPUT」欄位：

```
the color of the grass is
```

將下列文字新增至「OUTPUT」(輸出內容) 欄位：

```
the color of the grass is green
```

![image](https://github.com/user-attachments/assets/22fc73b7-1d77-4eca-a6c7-649cdf747ab1)

4. 點選頁面右側的「新增樣本」按鈕。

與預期不同，模型沒有接續完成句子，而是另外提供一個完整的句子。請試著使用單樣本提示來影響模型的回覆。這次加入一個樣本，供模型輸出內容時參考。

5. 在「測試」欄位，複製「撰寫輸入內容」欄位中的下列內容。
 In the Test field, copy the following in the Input field.

```
The color of the sky is
```

![image](https://github.com/user-attachments/assets/46173eba-7c68-475f-aad7-395939e458fd)


6. 點選頁面右側的「提交」按鈕。
   Click on the Submit button. You should receive a response from the model similar to the following:

```
The color of the sky is blue
```

注意：如果您國家/地區的拼字使用「colour」而非「color」，可以自行更改。

Instead of completing the sentence, the model gave a full sentence as a response since you provided an example for the model to base its output from. To change the response to simply complete the sentence, you can adjust the example provided in the OUTPUT field.


7. Click the Examples button in the Prompt box and change the OUTPUT field to:

```
Green
```
8. Click on the Add examples button.
9. In the Test field, copy the following in the Input field.
```
The color of the sky is
```

10. Click on the Submit button. You should receive a response from the model similar to the following:
![image](https://github.com/user-attachments/assets/60cbee3a-f7f1-409f-ad4a-ae5dcc152bd9)

You can see that the model now completes the sentence based on the example you provided. You have successfully influenced the way the model produces response.

#### 您已成功改變模型的回覆方式。

### Few-shot prompting


在下一個練習中，您將使用模型對句子執行情緒分析，例如判定電影評論為正面或負面。

1. 返回「文字提示」視窗。  
2. 點選「新增樣本」，然後在「示例」欄位中，刪除先前在「INPUT」和「OUTPUT」新增的 green grass 文字。  

模型並未取得充足資訊，無法得知您想執行情緒分析。您可以提供模型一些範例來調整回覆方式。

試著加入下圖中的範例：

![image](https://github.com/user-attachments/assets/14991e9e-a33e-48c7-9462-8b34fca50973)
![image](https://github.com/user-attachments/assets/f93ae9b2-a22f-4f3f-962c-84c2bd4641ff)

輸入內容	輸出內容
一部成功且有趣的電影	正面
10 分鐘後我就睡著了	負面
這部電影還可以	沒意見

然後點選頁面右側的「新增樣本」按鈕。

![image](https://github.com/user-attachments/assets/bf5d4979-ba61-4793-9626-4e3cd36f9b4a)

![image](https://github.com/user-attachments/assets/934afe72-2c4c-477d-9aab-a40ff8a1a25e)

![image](https://github.com/user-attachments/assets/5c760a42-cbff-4c85-88ca-3b41702a15ec)

![image](https://github.com/user-attachments/assets/5ec8f643-25f9-40a8-b9b1-8a3a31405d28)

### 工作 4：生成對話 Task 4. Generate conversations

您可以透過「建立聊天提示」享有任意形式的聊天體驗，模型會記錄說過的內容並根據情境回覆。
Chat mode is a conversational mode that allows you to have a freeform chat with the model. The model uses the conversation history as context for future responses. In this section, you will create a chat prompt and have a conversation with the model.

1. 從左選單前往「聊天」建立新的聊天提示。 From the left menu, navigate to Chat to create a new chat prompt.  

2. 「模型」請選取「gemini-1.5-flash-001」 On the top right under Model, select the gemini-1.5-flash model.  

Note: The model name and version may change with the release of new models.

3. Add the following context to the System instructions field by clicking the Edit button.

```
Your name is Roy.
You are a support technician of an IT department.
You only respond with "Have you tried turning it off and on again?" to any queries.
```







