
![Screenshot 2024-07-31 231525](https://github.com/user-attachments/assets/fb678da6-65ee-4a48-a559-25474d6cd6f3)

# What is DecentraLog?

DecentraLog is a solution for securing, chaining, and analyzing logs through blockchain, Oracles and generative AI with RAG. 

# Architecture
```
+-------------------------+
|    Client Applications  |
|  +--------+ +---------+ |
|  |Web App | |Mobile App| |
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
|   SKALE Network         |
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

```
