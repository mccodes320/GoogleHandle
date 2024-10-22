GSP519


工作 1：建構 Gemini 圖片分析工具

![image](https://github.com/user-attachments/assets/d07c16ac-8c5c-4b8e-a482-169f44b241e9)

![image](https://github.com/user-attachments/assets/2b42d3f6-883c-477b-b65a-6561c23bed5f)

![image](https://github.com/user-attachments/assets/157ecdae-0291-434c-8d6e-2a93ec7bda33)

![image](https://github.com/user-attachments/assets/54655cc0-8801-425e-9792-38e5389c22bc)

![image](https://github.com/user-attachments/assets/d81e6682-b875-4546-8582-cd40d965f9b6)

注意：請務必使用 gemini-1.5-pro 模型進行這項工作！

工作 2：建構 Gemini 標語生成器

在這項工作中，您將使用 Vertex AI Studio 的 Gemini 1.5 Pro 模型，建立任意形式提示來生成不同標語。工作目標是設計能自訂標語風格的提示，展現產品屬性、鎖定目標對象和引起情緒共鳴。

![image](https://github.com/user-attachments/assets/e41fb195-2dba-4236-a972-4fdd2dfcdff4)

![image](https://github.com/user-attachments/assets/aed61034-67ca-46d9-a232-f1c24f4dd0d4)



工作 3：試驗圖片分析程式碼

在這項工作中，您將針對自己建立的圖片分析提示，探索 Python 程式碼。接著將程式碼修改得更具體，並在筆記本中測試新提示。

1. 前往 Google Cloud 控制台，依序點按「導覽選單」>「Vertex AI」>「Workbench」。

2. 前往「執行個體」頁面，找到 generative-ai-jupyterlab 筆記本，然後點按「Open JupyterLab」按鈕。

![image](https://github.com/user-attachments/assets/763ff696-ca62-4914-b7b0-80bb772e9d40)

3. 建立新的筆記本檔案並命名為 image-analysis.ipynb。

![image](https://github.com/user-attachments/assets/ff6a0dc7-49cc-4187-9477-3e7e296a4b2b)

![image](https://github.com/user-attachments/assets/4dbf002c-a592-45cf-9aaa-7f7bbf5c4bad)

![image](https://github.com/user-attachments/assets/8fe696e4-796a-42b3-a758-62998fc83785)

![image](https://github.com/user-attachments/assets/183e866b-c647-438f-9897-a11f4fd870f0)

![image](https://github.com/user-attachments/assets/ff0064b4-eae3-415c-b0a0-ecd64afb261a)

![image](https://github.com/user-attachments/assets/7313d453-0234-4318-be30-f35b8c06903a)

![image](https://github.com/user-attachments/assets/f8bcb75f-144a-4849-8eef-893d3b082ea5)

![image](https://github.com/user-attachments/assets/822a8308-115c-476f-b4e8-bd49d9657e03)

![image](https://github.com/user-attachments/assets/f450a4b4-771f-4252-bfe4-c77f3b89bb1c)


工作 4：試驗生成標語的程式碼



```
from vertexai.preview.generative_models import GenerativeModel

model = GenerativeModel("gemini-1.5-pro")

prompt = """
Cymbal Direct is partnering with an outdoor gear retailer. They\'re launching a new line of products designed to encourage young people to explore the outdoors. Help them create catchy taglines for this product line.

input: <Write a tagline for a durable backpack designed for hikers that makes them feel prepared. Consider styles like minimalist.>
output: <Built for the Journey: Your Adventure Essentials.>

input: nature
output: nature

input: <your test input>
output:

last input: specifically request that the tagline includes the keyword nature
"""

responses = model.generate_content(
    prompt,
    generation_config={
        "temperature": 1,
        "max_output_tokens": 2048,
        "top_p": 1.0,
        "top_k": 40,
    },
    stream=True
    )

for response in responses:
    print(response.text)
```

output
```
Here
 are some taglines for a durable backpack designed for hikers, incorporating the keyword "
nature":

**Short & Sweet:**

* **Nature Ready:**  Simple
, clear, and emphasizes preparedness.
* **Built for Nature:** Emphasizes durability and suitability for outdoor use.
* **Carry Your Nature:** Connects
 the backpack to the experience of being in nature.

**More Descriptive:**

* **Embrace Nature: Gear Up and Explore.**  Action-oriented and inviting
.
* **Your Nature Escape: Pack It In.**  Focuses on the feeling of getting away.
* **Find Your Path: Nature Essentials Included.**  Highlights both the backpack and the experience.
```

