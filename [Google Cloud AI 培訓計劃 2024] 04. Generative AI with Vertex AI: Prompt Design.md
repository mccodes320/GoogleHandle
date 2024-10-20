### Generative AI with Vertex AI: Prompt Design

GSP1151

Overview
This notebook covers the essentials of prompt engineering, including some best practices.

Learn more about prompt design in the official documentation.

In this lab, you learn best practices around prompt engineering -- how to design prompts to improve the quality of your responses.

This notebook covers the following best practices for prompt engineering:

*簡潔 Be concise  
*具體且明確 Be specific and well-defined  
*一次詢問一項任務 Ask one task at a time  
*將生成任務轉換為分類任務 Turn generative tasks into classification tasks  
*透過包含範例來提高響應質量 Improve response quality by including examples  

### Prerequisites

Before starting this lab, you should have familiarity with the following concepts:  

*Basic understanding of Python programming
*General knowledge of how APIs work
*Running Python code in a Jupyter notebook in Vertex AI Workbench
https://cloud.google.com/vertex-ai/docs/workbench/introduction

### Objectives:
In this lab you will learn how to:

*Get started with prompt engineering with the Vertex AI SDK:  
*Best practices  

How to explore some text generation use cases with the Vertex AI SDK:  

*構思Ideation  
*問答Q&A  
*文字分類 Text classification  
*文字擷取 Text extraction  
*文字摘要 Text summarization    

### Setup and requirements

### Task 1. Open the notebook in Vertex AI Workbench

1. In the Google Cloud Console, on the Navigation menu, click Vertex AI > Workbench.

2. Find the vertex-ai-jupyterlab instance and click on the Open JupyterLab button.

The JupyterLab interface for your Workbench instance will open in a new browser tab.

![image](https://github.com/user-attachments/assets/a93b6feb-e311-47fd-8186-c89cb8f70240)
![image](https://github.com/user-attachments/assets/16933cb4-764e-403f-8024-ded258837ef1)

### Task 2. Set up the notebook

1. Click on the intro_prompt_design file.

2. Run through the Prompt engineering best practices section of the notebook.

* For Project ID, use qwiklabs-gcp-02-dd1ad620be77, and for the Location, use us-west1.

![image](https://github.com/user-attachments/assets/59e3f647-4e26-4925-9838-44a471db781d)
![image](https://github.com/user-attachments/assets/32cfac5f-f7b8-45a7-acec-3088215b8bf0)

點擊“檢查我的進度”以驗證目標。安裝套件並導入庫。Install packages and import libraries.
點擊“檢查我的進度”以驗證目標。保持簡潔。Be concise.
點擊“檢查我的進度”以驗證目標。要具體、明確。Be specific, and well-defined.
點擊“檢查我的進度”以驗證目標。一次詢問一項任務。Ask one task at a time.
點擊“檢查我的進度”以驗證目標。小心出現幻覺。Watch out for hallucinations.





Click Check my progress to verify the objective.
![image](https://github.com/user-attachments/assets/78e318cc-2463-4992-a3fc-d18b76fb5fa1)

Click Check my progress to verify the objective.





### Task 3. 減少輸出變化 Reduce Output Variability

Run through the Turn generative tasks into classification tasks to reduce output variability section of the notebook.

Click Check my progress to verify the objective.

生成性任務會導致更高的輸出變化。 Generative tasks lead to higher output variability.

分類任務減少了輸出的可變性。 Classification tasks reduces output variability.




### Task 4. 透過包含範例來提高回應質量 Improve Response Quality by Including Examples









