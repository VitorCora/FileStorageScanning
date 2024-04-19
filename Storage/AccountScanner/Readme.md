# FileStorageScanning

# New Architecture

Utilizing Cloud Vision One Account achitecture

In this scenario we will be using a Prefixes (folder strucutre) in the Landing Bucket, this structure can be leveraged for scanning decision.

Files will only be scanned when they are uploaded to the SCAN prefix of the specified buckets, objects will be scanned if they are moved between folders

Bucket/Buckets to be scanned:


![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/cff4a335-48c3-438d-aa00-870575c1c32e)

----

![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/7ab1628a-9e4d-40d1-8943-d061f2f7e148)

You will also need to enable 

 ## How to Deploy

 - Log into Vision One
 - Go to the Service Management Page
 - On the Service Management page select the Cloud Accounts service
 - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/ac9e89c1-10b0-4d28-b7e7-f27cccb61b47)
  - On the Cloud Services page, click on **Add Account**
   - Give a name to your new account
   - Select the region where you will deploy the Stack
   - Core Feature comes enabled by default
   - Enable File Security Storage
   - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/b077c6d5-262b-4e8f-afe4-08fd30eb3ca5)
   - Click in Lauch
   - On AWS run the stack
   - After the stack integration is done, just wait and it should quickly appear on your V1 console
   - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/0a698e00-bfda-4732-a698-665b0bfdeefc)
   - Now go to the **Cloud Security Page** and Select **File Security**
    - On Iventory, select **AWS** and expand your newly integrated AWS Account
    - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/e86d7771-1c73-480a-b51b-03e52c0ea851)
    - Tick the Bucket that you want to protect and click on **Change Status** **Turn on EventBridge**
     - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/4696ffad-0a20-4572-862b-977569fbd60e)
     - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/827d3117-885f-42c8-955b-245c01739ef3)


  



