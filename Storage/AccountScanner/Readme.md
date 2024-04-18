# FileStorageScanning

# Second Architecture

Utilizing Cloud One/Vision One Account achitecture

In this scenario we will be using a Prefixes (folder strucutre) in the Landing Bucket, this structure can be leveraged for scanning decision.

Files will only be scanned when they are uploaded to the SCAN prefix of the specified buckets, objects will be scanned if they are moved between folders

Bucket/Buckets to be scanned:


![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/cff4a335-48c3-438d-aa00-870575c1c32e)

----

![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/7ab1628a-9e4d-40d1-8943-d061f2f7e148)

You will also need to enable 

 ## How to Deploy

 - Log into Cloud One
 - Generate an API Key
   - Go to the Administration page
   - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/c2e13c2b-1bf5-4833-88aa-b0cfa628437d)
   - Look for the API Keys Section:
   - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/bc6e411e-cc6b-4c6d-89be-7f0a79c3361b)
   - In the API Keys Section, Click on **New**
   - Give it an **Alias** and select **Full Access** for Role and then Click **Next**
   - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/012b19e9-32ab-45df-9af8-c279f7cf534f)
   - Copy the API Key
  
   - Acquire the CreateStackURL:
     -  Method: GET
     -  Endpoint:  https://filestorage.{region}.cloudone.trendmicro.com/api/templates/{provider-type}
       - region = Your Cloud One region {us-1, eu-1, ...}
       - provider-type =  aws-account-scanner
      - Headers:
        - Authorization: ApiKey {YOUR API KEY}
        -  Api-Version: v1
     -  ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/04e7ce64-9b0b-4ebb-a18c-dc442115f3ee)
  - Expected Response:
   - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/2228066c-9a42-4422-92a0-8b6067e45f3b)

- Run the Cloudformation URL
- ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/3627f8aa-4503-42de-9174-d2bb22054181)
- ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/9bec28f0-48e4-4059-963d-75de1a0d6d14)
- ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/b2219bc2-a3ea-4e81-a240-a510bbe0f788)
- ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/e246bd52-216b-458e-92f8-bd5c6042f30e)
