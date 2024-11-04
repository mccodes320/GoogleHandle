Develop an app with Gemini

Task 1. Configure your environment and account

![image](https://github.com/user-attachments/assets/57f49169-2337-4213-8f18-d76f2c988a63)

Task 2. Create a Cloud Workstation 工作 2：建立雲端工作站

This lab uses Gemini assistance to develop an app with the Cloud Code plugin for Cloud Workstations IDE. Cloud Workstations is a fully managed integrated development environment that includes native integration with Gemini.

In this task, you configure and provision your Cloud Workstation environment, and you enable the Cloud Code plugin for Gemini.

View the workstation cluster
A workstation cluster named my-cluster has been pre-created for this lab. This cluster is used to configure and create a workstation.

1. In the Google Cloud console, select the Navigation menu (Navigation menu icon), and then select View All Products > Tools > Cloud Workstations.  
2. In the Navigation pane, click Cluster management.  
3. Check the Status of the cluster. If the status of the cluster is Reconciling or Updating, periodically refresh and wait until it becomes Ready before moving to the next step.  


![image](https://github.com/user-attachments/assets/6df943c5-fd43-4d82-b88a-c2952b25e7cb)
![image](https://github.com/user-attachments/assets/7c5fc18c-25d0-4d5e-b9a2-63cf2f967c6c)

Create a workstation configuration

Before creating a workstation, you must create a workstation configuration in Cloud Workstations.

In the Navigation pane, click Workstation configurations, and then click Create Workstation Configuration.

Specify the following values:

![image](https://github.com/user-attachments/assets/e964a872-2c9f-4e06-bdf2-fee6ba86611c)

Click Create.

Click Refresh.

Check the Status of the configuration being created. If the status of the configuration is Reconciling or Updating, periodically refresh and wait until the status becomes Ready before moving to the next step.

![image](https://github.com/user-attachments/assets/45d6cf8c-d75b-4639-ad27-bd6b76fdf340)

![image](https://github.com/user-attachments/assets/0c88b25f-04a4-4923-9c5f-9272e4d24d38)

![image](https://github.com/user-attachments/assets/bf55a624-b925-4d77-8d5c-f7b4dfe3ea6e)

![image](https://github.com/user-attachments/assets/43997ff9-364a-4c67-9028-1835d5c9c1d1)

![image](https://github.com/user-attachments/assets/c4ba55e9-ba7c-49b2-8665-db0f05031396)

![image](https://github.com/user-attachments/assets/fa3554cf-d9af-4354-a82f-c45ae61b9e0b)

![image](https://github.com/user-attachments/assets/2a6ba5fc-bbca-4609-817e-262640a263e7)

![image](https://github.com/user-attachments/assets/790e66b9-f2c6-49e4-9a69-bf5ad9dc8ba9)

![image](https://github.com/user-attachments/assets/10a34a87-c903-44ea-8c6a-d9beff3dc1d4)

啟動 IDE
為了確保正常運作，部分擴充功能需要啟用瀏覽器中的第三方 Cookie。

如要在 Chrome 啟用第三方 Cookie，請點按 Chrome 選單中的「設定」。

在搜尋列輸入「第三方 Cookie」。

點按「第三方 Cookie」設定，然後選取「允許第三方 Cookie」。

注意：本研究室活動結束後，如要還原瀏覽器目前的設定，請記下原本的第三方 Cookie 設定。
在 Google Cloud 控制台的「工作站」頁面中點按「啟動」，即可啟動工作站的 Code OSS IDE。

IDE 會在新的瀏覽器分頁中開啟。

![image](https://github.com/user-attachments/assets/f90f73a8-5b2f-4cb7-a14e-d9b57a7345a9)
![image](https://github.com/user-attachments/assets/e9fa9275-8fa7-4951-880a-8aadc4859b6f)

工作 3：更新 Cloud Code 擴充功能以啟用 Gemini
在這項工作中，您將啟用 Cloud Code 中的 Gemini，並用於工作站 IDE。

連結至 Google Cloud
請按照以下步驟，將工作站連結至 Google Cloud：

在視窗底部點按狀態列上的「Cloud Code - Sign In」。
![image](https://github.com/user-attachments/assets/cee9fa85-e9de-4261-8971-5269fd8f82c7)

如果系統提示您登入，請點按「Proceed to sign in」。

終端機會顯示連結。

按下 Control 鍵 (Windows 和 Linux)/Command 鍵 (MacOS)，並點按終端機中的連結，即可啟動 Cloud Cloud 登入流程。

如果系統向您確認是否要開啟外部網站，請點按「開啟」。

點按學生電子郵件地址。

系統提示您繼續操作時，請點按「繼續」。

如要讓 Google Cloud SDK 存取您的 Google 帳戶，請詳閱並同意相關條款，然後點按「允許」。

瀏覽器分頁會顯示您的驗證碼。

點按「複製」。

返回 IDE，在終端機中顯示「輸入授權碼」的位置貼上驗證碼。

如果系統要求您允許從剪貼簿複製，請點按「允許」。

點按「輸入」，然後等候狀態列顯示「Cloud Code - No Project」。

您已連結到 Google Cloud。
















































