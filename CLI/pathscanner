# API/SDK Scanning

## Scan all the images on a $PATH (folder)

This scenario is focused in covering on demand malware scan for all the most common software images hosted on a path.

You will have the capability to scan files using a simple CLI invocation or one of our many SDKs.

This method does not requires you to integrate your Cloud account to Vision One.

- How to create the Vision One API that will be used on the
  - Log into Vision One.
  - On the Vision One Console go to the **Administration** Page and select the **User Roles** Service:
    - Click on **+Add Role**
    - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/507febba-7b19-4d7c-b45f-4cdc1daf6556)
    - On the **Create Custom Role** Page
    - Under General Information:
      - Choose a **Role Name**: eg. v1fs-sdk-role.
      - Add a **Role Description**: eg. Role to enable SaaS malware scan to be performed
      - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/5ee998c8-744a-4eea-ad4d-b284d6064cfb)
    - Under Permission, select only
      -   Under **Security Functions**
        - Expand **Cloud Security**
          - Expand **File Security**
            - Tick View
            - Tick Run file scan via SDK
            - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/1149bb2e-ff99-41c5-865b-eb100d13e8e7)
    - Click **Save**
  - On the Vision One Console go to the **Administration** Page and select the **API Keys** Service:
    - Click on **Add API Key**
    - Choose a **Name**: eg. v1fs-sdk-api.
    - Choose the recently created role: eg. v1fs-sdk-api.
    - Set an **Expiration time**
    - Choose a **Description** (Optional): eg. API Key to enable SaaS malware scan to be performed 
      - Add a **Role Description**: eg. API Key to enable SaaS malware scan to be performed
      - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/888e4704-b4f9-4a21-8d9f-5bfe6bf1ed22)
      - Click **Add**
  - Copy the given API and store it properly 

- How access the SaaS file Scan (SDK/API) results and guides:
  - Log into Vision One.
  - On the Vision One Console go to the **Cloud Security** Page and select the **File Storage** Service:
  - Click on the SDK Icon
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/c82f22ff-b679-4bab-8646-100a9f1593c8)
  - https://portal.xdr.trendmicro.com/index.html#/app/file-security
  - For the results go to the **Scan Activity** Tab
  - ![image](https://github.com/VitorCora/FileStorageScanning/assets/59590152/56f4c454-0974-416f-8e1a-4c12c5eeaf68)

# Using the NodeJS sdk

This scenario is focused in covering on demand malware scan by using the NodeJS SDK.

Reference:
https://github.com/trendmicro/tm-v1-fs-nodejs-sdk

Based on the following documentation I changed the SDK to run with files and Pre-signed URLs or download Links:

Reference:
https://github.com/VitorCora/tm-v1-fs-nodejs-sdk

You can fork this documentation and change it to your specific use case.

This guide will be using the example package called fScan.ts, that live in the following link:
https://github.com/VitorCora/tm-v1-fs-nodejs-sdk/blob/main/examples/cli/src/fScan.ts

This NodeJS program after compiled will run with the following command line:

npm run client -- (-f #FILEPATH or -u $URL) --pml (true or false) --smt (true or false)

Where:

-f #FILEPATH is the path to the file to be scanned

-u #URL is the URL or pre-signed URL

-pml is the predictive machine learning (recomended to always be set to "true")

-smt is the parameter for the smart feedback (recommended to always be set to "true")

  Trend Micro™ Smart Feedback provides continuous communication between Trend Micro products as well as the company's 24/7 threat research centers and technologies. Each new threat identified through a single customer's routine reputation check automatically updates   all Trend Micro threat databases, blocking any subsequent customer encounters of a given threat.
  
  REference:
  https://docs.trendmicro.com/all/ent/sps/v3.2/en-us/sps_olh/Smart-Feedback.html

It is only needed -f #FILEPATH or -u $URL, in the case of both being supplied the scanner will give preference to the -f #FILEPATH

## Installing the SDK
  
  1. To install the SDK's Node.js package, run the following commands in your Node.js application folder.

  npm install file-security-sdk

  2. On the host:

  git clone https://github.com/VitorCora/tm-v1-fs-nodejs-sdk.git

  cd cli/

  export TM_AM_SERVER_ADDR={YOUR_VISION_ONE_API_KEY_REGION}
  export TM_AM_AUTH_KEY={YOUR_VISION_ONE_API_KEY}

  Where:

   
  {YOUR_VISION_ONE_API_KEY_REGION} Will be your Vision One region, if you have a US console use **us-east-1**
  {YOUR_VISION_ONE_API_KEY} Will be the API Key created previously **(eg. the copied value from v1fs-sdk-api)**
  
  If you want to set up the Logging Level, set the following variable:

  export TM_AM_LOG_LEVEL={LOG_LEVEL}

  Where:

  {LOG_LEVEL} Valid values are **OFF, FATAL, ERROR, WARN, INFO**, and **DEBUG**; default level is OFF

Install your dependencies:

npm install

Build the example, setting your Source to fScan.ts(Scan files or PresignedURLs or downloadable files):

SOURCE=fScan.ts npm run build # cli

Feed the files or Pre-signed URLs that will be scanned:

npm run client -- (-f #FILEPATH or -u $URL) --pml (true or false) --smt (true or false)

*** Testing an eicar .png

  - ![image](https://github.com/VitorCora/tm-v1-fs-nodejs-sdk/assets/59590152/32231f0f-c8b6-4bfa-b8b6-c269a020bc26)

*** Testing a random eicar.txt

   - ![image](https://github.com/VitorCora/tm-v1-fs-nodejs-sdk/assets/59590152/e970949e-5a27-4140-8095-a5063197202a)


*** Testing a presigned URL

![image](https://github.com/VitorCora/tm-v1-fs-nodejs-sdk/assets/59590152/af0b8702-7208-40a0-8237-7566e673b61d)



