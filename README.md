d8888b.      d88888b       .o88b.      d88888b      d8b   db      d8888b.       .d8b.       db            .d88b.        d888b  
88  `8D      88'          d8P  Y8      88'          888o  88      88  `8D      d8' `8b      88           .8P  Y8.      88' Y8b 
88   88      88ooooo      8P           88ooooo      88V8o 88      88oobY'      88ooo88      88           88    88      88      
88   88      88~~~~~      8b           88~~~~~      88 V8o88      88`8b        88~~~88      88           88    88      88  ooo 
88  .8D      88.          Y8b  d8      88.          88  V888      88 `88.      88   88      88booo.      `8b  d8'      88. ~8~ 
Y8888D'      Y88888P       `Y88P'      Y88888P      VP   V8P      88   YD      YP   YP      Y88888P       `Y88P'        Y888P  

Securing, chaining, and analyzing logs through blockchain, Oracles and generative AI with RAG.


# Architecture

+-------------------------+
|    Client Applications  |
|  +--------+ +---------+ |
|  |Web App | |Mobile App||
|  +--------+ +---------+ |
+------------+------------+
             |
             | HTTPS/WSS
             v
+-------------------------+
|   AWS CloudFront        |
| (Content Delivery)      |
+------------+------------+
             |
             v
+-------------------------+
|   AWS Amplify           |
| (Hosting & Deployment)  |
+------------+------------+
             |
             v
+-------------------------+
|   API Gateway / LB      |
+------------+------------+
             |
     +-------+-------+
     |               |
     v               v
+------------+ +------------+
|NestJS      | |WebSocket   |
|Server      | |Gateway     |
+------------+ +------------+
     |               |
     +-------+-------+
             |
             v
+-------------------------+
|   NestJS Application    |
| +---------------------+ |
| | Controllers         | |
| | Services            | |
| | Modules             | |
| | Middleware          | |
+------------+------------+
     |               |
     v               v
+------------+ +------------+
|Database    | |Cache       |
|(RDS/Dynamo)| |(ElastiCache|
+------------+ +------------+
             |
             v
+-------------------------+
| DApp Development Tools  |
| +---------------------+ |
| | Truffle Suite       | |
| | Web3.js / ethers.js | |
+------------+------------+
             |
             v
+-------------------------+
| AWS Blockchain Services |
| +---------------------+ |
| | Amazon EC2          | |
| | (Layer 2 Nodes)     | |
| +---------------------+ |
| | Amazon S3           | |
| | (Data Storage)      | |
| +---------------------+ |
| | AWS Lambda          | |
| | (Serverless Compute)| |
| +---------------------+ |
| | Amazon VPC          | |
| | (Networking)        | |
| +---------------------+ |
| | Amazon QLDB         | |
| | (Ledger Database)   | |
+------------+------------+
             |
             v
+-------------------------+
| Cloud DevOps Services   |
| +---------------------+ |
| | AWS CodePipeline    | |
| | AWS CodeBuild       | |
| | AWS CodeDeploy      | |
+------------+------------+
             |
             v
+-------------------------+
|   Ethereum Network      |
|  +-------------------+  |
|  |  Smart Contract   |  |
|  | (SecurityLogs.sol)|  |
|  +-------------------+  |
+------------+------------+
     |               |
     v               v
+------------+ +------------+
|Chainlink   | |External    |
|Oracle      | |Data Sources|
+------------+ +------------+
     |               |
     +-------+-------+
             |
             v
+-------------------------+
|   RAG System            |
| +---------------------+ |
| |Document Retriever   | |
| |Perplexity AI        | |
| |Log Analyzer         | |
+------------+------------+
             |
             v
+-------------------------+
|   Alert System          |
+-------------------------+
