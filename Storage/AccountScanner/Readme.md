# FileStorageScanning

# New Architecture

Utilizing Vision One Account achitecture

In this scenario we will be using Prefixes to decide the files to be scanned.

Files will only be scanned when they are uploaded to the chosen bucket and its key (name) has the SCAN prefix.

Bucket/Buckets to be scanned:

![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/a30e7286-9728-4d63-af0b-a04403a95c7b)


----

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
    - At the Parameters page, fill the following:
     - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/42a335a7-f208-4107-ab28-26e0fd58e085)
     - FileSecurityStorageObjectCreatedEventFilter
        "bucket": {"name": [{"prefix": "yourbucket-to-scan"}]},"object": {"key": [{"prefix": "scan"}]}},  
      - or
        "object": {"key": [{"prefix": "scan"}]}}
      - Where:
       - **{yourbucket-to-scan}** is the name of the bucket to be scanned
       - **{scan}** is the prefix of the objects that you want to scan
   - After the stack integration is done, just wait and it should quickly appear on your V1 console
   - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/0a698e00-bfda-4732-a698-665b0bfdeefc)
   - Now go to the **Cloud Security Page** and Select **File Security**
    - On Iventory, select **AWS** and expand your newly integrated AWS Account
    - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/e86d7771-1c73-480a-b51b-03e52c0ea851)
    - Tick the Bucket that you want to protect and click on **Change Status** **Turn on EventBridge**
     - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/4696ffad-0a20-4572-862b-977569fbd60e)
     - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/827d3117-885f-42c8-955b-245c01739ef3)


  ## AWS Event Bridge




{ "detail-type": 

  ["Object Created"], 
  
  "source": ["aws.s3"], 
  
  "detail": { 
  
    "bucket": { 
    
      "name": [{ 
      
        "prefix": "yourbucket-to-scan" 
        
      }] 
     
     },
    
    "object": { 
      
      "key": [{
        
        "prefix": "scan" 
      
      }] 
    
    } 
  }, 
  
  "resources": [{
    
    "anything-but": ["your-bucket-not-to-scan-1", "your-bucket-not-to-scan-2", "your-bucket-not-to-scan-3"] 
  
  }] 

}

![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/59bab939-a1ad-4dd8-8002-a93fe1884e81)


## Tests

The tests were conducted utilizing a clean image of my dog:
![Robin RG](https://github.com/VitorCora/FileStorageScanning/assets/59590152/9ebc9258-82e2-44a5-8dc7-543a6ff74826)

I changed the Image name to scanRobin RG.jpeg and Robin RG.jpeg to test the different possible behaviors of the scan engine and AWS EventBridge.
  
## Results

Upload of the Image named scanRobin RG.jpeg

Object information:

![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/d1d3794d-d941-4884-be2d-3eabef774a0b)

Object TAG metadata:

![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/760cd8ad-135e-4c39-bfc3-313a845ae0e1)

Upload of the Image named Robin RG.jpeg:

Object TAG metadata:

![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/497c8bca-b174-4de4-973e-b65e6a575fe5)

Object information:

![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/a1ff1303-7742-440f-b592-1f294e47ace4)


## Notes

After extensive tests, EventBridge is still firing for object prefix, even with the use of "object": {"key": "anything-but":"string"} , "object": {"key": [{"anything-but": {"prefix": "string"}}]} and many other combinations.






