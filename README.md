🧪 Trello REST API Testing Project
This project demonstrates manual and automated API testing workflows using Trello's REST API. It simulates CRUD operations across Boards, Lists, and Cards, covering realistic dependency chains and ensuring the reliability of Trello-like task management systems.

📋 Project Overview
The goal of this project is to ensure the correct functioning of Trello APIs by validating the lifecycle of objects (Board → List → Card) using structured dependencies. Each operation is executed based on the logical data flow and interdependency between resources.

🔧 Dependencies
All API requests are designed with realistic dependencies between endpoints. The chart below shows the logical execution order and prerequisites for each operation:

⚙️ Each test case includes API endpoint, HTTP method, request body, assertion logic, and dependency handling.

🛠️ Tools Used
Postman / REST Client – for request execution and collection testing

Trello REST API – official Trello endpoints

Environment Variables – for storing API keys and tokens securely

JSON – for structured request bodies

Manual + Automated Testing – hybrid testing style

📁 Test Structure
The test suite includes the following:

/Trello-API-Testing
│
├── Boards/
│   ├── Create_Board.json
│   ├── Get_Board.json
│   ├── Update_Board.json
│   └── Delete_Board.json
│
├── Lists/
│   ├── Create_List.json
│   ├── Get_List.json
│   ├── Update_List.json
│   └── Delete_List.json
│
├── Cards/
│   ├── Create_Card.json
│   ├── Get_Card.json
│   ├── Update_Card.json
│   └── Delete_Card.json
│
└── Environment/
    └── TrelloEnvironment.postman_environment.json

🔗 API Operations and Their Dependencies

📁 Board Operations

Operation	Dependency Flow
Create Board	    None
Get Board	        Create Board → Get Board
Update Board	    Create Board → Update Board → Get Board
Delete Board	    Create Board → Update Board → Delete Board → Get Board

📂 List Operations
Operation	Dependency Flow
Create List	Create Board → Get Board
Get List	Create List → Get List
Update List	Create List → Update List → Get List
Delete List	Create List → Update Card → Delete List → Get List

🗂️ Card Operations
Operation	Dependency Flow
Create Card	Create List → Get Card
Get Card	Create Card → Get Card
Update Card	Create Card → Update Card → Get Card
Delete Card	Create Card → Delete Card → Get Card

🚀 Getting Started

Clone this repo

Import the collection and environment into Postman

Add your Trello API Key and Token to the environment variables

Run tests in sequence based on dependencies

📌 Requirements
Trello API Key & Token – Get from Trello API Docs

Postman or REST Client
