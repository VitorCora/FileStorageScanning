# FileStorageScanning

# First Architecture

Utilizing Cloud One traditional deployment method + Prefixes

In this scenario we will be using a Prefixes (folder strucutre) in the Landing Bucket, this structure can be leveraged for scanning decision.

Files will only be scanned when they are uploaded to the SCAN bucket, objects will be scanned if they are moved between folders

Prefixes (Folder Structure):
  - Scan
  - Do-NOT-Scan
  ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/046219a7-7562-49d8-992f-042676b8691d)

## Add Flow and architecture here
----- 


## First Scenario, upload a clean image to the Bucket main.
  - A clean picture of my dog
  - ![Robin RG](https://github.com/VitorCora/FileStorageScanning/assets/59590152/78d7a86d-f13d-453e-8805-a75212d5451f)
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/c6a7d376-edbd-4ac9-80e9-f7a75500e22e)
  - Object metadata
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/299949f7-2e94-49ea-acb6-72e257257b4e)
  - Tag Section
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/3b2de559-ce0c-41bf-ae98-f98c75ff25c6)

----

## Second Scenario, upload a clean image to the Bucket, Do-Not-Scan Prefix (Folder):
  -  A clean picture of my dog
  -  ![Robin RG](https://github.com/VitorCora/FileStorageScanning/assets/59590152/e1427357-a2a9-4fe3-b2a8-676ffb36e33b)
  -  ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/aad7abea-28dd-465f-8915-46a983d48350)
  -  Object Metadata
  -  ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/bc5670a7-bc2f-4936-bba7-155cdbe9d818)
  -  Tag Section
  -  ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/615e6b6e-7506-4dfe-9847-5d65dc74f2ed)

-----

## Third Scenario, upload a clean image to the Bucket, Scan Prefix (Folder):
  - A clean picture of my dog
  - ![Robin RG](https://github.com/VitorCora/FileStorageScanning/assets/59590152/101f5914-1598-4bc3-b092-6c660fa971a1)
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/448ffa83-07d0-4a05-836c-8c8e94212fc7)
  - Object Metadata
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/a3a9d9b6-40c6-4269-abfa-054dba220637)
  - Tag Section:
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/3428f011-da99-4c17-81a5-a0d937ca40f9)

----

## Fourth Scenario, upload a malicious file to the Bucket, Scan Prefix (Folder):
  - A malicious eicar file
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/0f9d3fe6-d0b9-4bb9-bd0f-e44c8cef4ca0)
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/448ffa83-07d0-4a05-836c-8c8e94212fc7)
  - Object Metadata
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/5fbdf772-5de8-4c39-992b-754b9d932512)
  - Tag Section:
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/7ada174d-727b-4cc8-865b-b96900e3828c)

----

## Fifth Scenario, upload a malicious file to the Bucket main, move the file to the Scan Prefix (Folder):
  - A malicious eicar file
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/d00c2a95-1db6-4478-adc4-c82f32d7206a)
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/67f92fd3-b276-4032-b0e6-2e6bcd590b65)
  - Object Metadata
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/555bcdba-316e-4738-afee-7e0a5cf58386)
  - Tag Section:
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/21c7adf2-4e9b-4eb3-ba0c-f470b740254d)
  - Moving the file:
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/085acaaa-b86b-4184-934c-306df0c89986)
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/ecd35fe8-31be-41bc-b083-ac4966a8cbdc)
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/330b38ca-7c73-4fc4-b4cd-66c625290524)
  - Object Metadata
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/8864c23c-b17e-4553-99c0-d3e3c224e06a)
  - Tag Section:
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/d5580bdf-f247-4877-9f59-b85874ee1bf1)

-----
## Results on the Cloud One Console

![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/497875d3-760d-498d-98e5-ba2c324b89b1)


 ## How to deploy

Under construction

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


![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/2a04439f-8f53-4239-8340-1a78964a59e1)


![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/46bec4ce-276e-479a-b9d2-bd7e7c05ff32)
