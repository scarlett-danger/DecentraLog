# DecentraLog
Securing, chaining, and analyzing logs through blockchain, Oracles and generative AI with RAG.

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
|   API Gateway / LB      |
+------------+------------+
             |
     +-------+-------+
     |               |
     v               v
+------------+ +------------+
|Web Server  | |WebSocket   |
|(Express.js)| |Server      |
+------------+ +------------+
     |               |
     +-------+-------+
             |
             v
+-------------------------+
|   Application Server    |
|   (Node.js/Python)      |
+------------+------------+
     |               |
     v               v
+------------+ +------------+
|Database    | |Cache       |
|(PostgreSQL)| |(Redis)     |
+------------+ +------------+
     |               |
     +-------+-------+
             |
             v
+-------------------------+
|   Blockchain Interface  |
|   (Web3.js/ethers.js)   |
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
             |
     +-------+-------+
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
| +---------------------+ |
| |Perplexity AI        | |
| |Log Analyzer         | |
| +---------------------+ |
+------------+------------+
             |
             v
+-------------------------+
|   Alert System          |
+-------------------------+

