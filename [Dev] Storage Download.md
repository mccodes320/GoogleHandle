
![image](https://github.com/user-attachments/assets/571b9c15-4d80-4472-9a3e-78389599bbe1)

![image](https://github.com/user-attachments/assets/b696e73e-fa6a-45cc-9e28-1994f6d9645d)

角色
環境和 Storage 物件檢視者

![image](https://github.com/user-attachments/assets/197d84e3-8843-4229-aa7e-df2f065697d1)

![image](https://github.com/user-attachments/assets/6a2e0d29-0604-4da3-9201-4e4d4aff221f)

![image](https://github.com/user-attachments/assets/9471f937-9074-4a29-bbc5-4f081a3eba45)


建立Storage

![image](https://github.com/user-attachments/assets/83cefd24-cec7-40c7-9012-3a589bf9ced6)


```
package test;

import java.io.IOException;
import java.nio.file.Paths;

import com.google.auth.oauth2.GoogleCredentials;
import com.google.cloud.storage.Blob;
import com.google.cloud.storage.BlobId;
import com.google.cloud.storage.Storage;
import com.google.cloud.storage.StorageOptions;

/**
 * 
 * Google Storage Download, use iam key
 * @author Macro
 *
 */
public class DownloadObject {
   public static void main(String[] args) throws IOException {
      // The ID of your GCP project
      String projectId = "unified-runner-411615";

      // The ID of your GCS bucket
      String bucketName = "gatag";

      // The ID of your GCS object
      String objectName = "access.log";

      // The path to which the file should be downloaded
      String destFilePath = "./file.txt";

      downloadObject(projectId, bucketName, objectName, destFilePath);
   }
   
   public static void downloadObject(String projectId, String bucketName, String objectName, String filePath)
         throws IOException {

       // Replace with the path to your service account JSON key file
       String serviceAccountKeyPath = "unified-runner-411615-878eadd35f7d.json";

       // Read service account credentials
       GoogleCredentials credentials = GoogleCredentials
           .fromStream(Paths.get(serviceAccountKeyPath).toFile().toURI().toURL().openStream());

       // Build Storage service
       Storage storage = StorageOptions.newBuilder().setProjectId(projectId).setCredentials(credentials).build()
           .getService();

       // Check if the object exists before downloading
       Blob blob = storage.get(BlobId.of(bucketName, objectName));
       if (blob == null) {
         System.err.println("Object not found: " + objectName);
         return;
       }

       blob.downloadTo(Paths.get(filePath));
     }
}
```
```
<project xmlns="http://maven.apache.org/POM/4.0.0"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<groupId>test</groupId>
	<artifactId>test</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<build>
		<sourceDirectory>src</sourceDirectory>
		<plugins>
			<plugin>
				<artifactId>maven-compiler-plugin</artifactId>
				<version>3.8.1</version>
				<configuration>
					<release>16</release>
				</configuration>
			</plugin>
		</plugins>
	</build>
	<dependencies>
		<!-- https://mvnrepository.com/artifact/com.google.cloud/google-cloud-storage -->
		<dependency>
			<groupId>com.google.cloud</groupId>
			<artifactId>google-cloud-storage</artifactId>
			<version>2.34.0</version>
		</dependency>
		<!-- Search -->
		<!-- https://mvnrepository.com/artifact/com.google.cloud/google-cloud-discoveryengine -->
		<dependency>
			<groupId>com.google.cloud</groupId>
			<artifactId>google-cloud-discoveryengine</artifactId>
			<version>0.37.0</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/com.google.cloud/google-cloud-security-private-ca -->
		<dependency>
			<groupId>com.google.cloud</groupId>
			<artifactId>google-cloud-security-private-ca</artifactId>
			<version>2.42.0</version>
		</dependency>
<dependency>
    <groupId>com.google.api-client</groupId>
    <artifactId>google-api-client</artifactId>
    <version>2.4.0</version>
</dependency>

	</dependencies>
</project>
```


