🏗️ Crowdfunding DApp

A decentralized crowdfunding platform built on Ethereum using Solidity, Hardhat, and a Next.js frontend. It allows users to create projects, contribute ETH, and handle fund withdrawals with contributor approval.

⸻

🚀 Features
• 🧑‍💼 Anyone can create a fundraising project
• 💸 Contributors can fund active projects
• ⏰ Projects automatically expire after a deadline
• ✅ Projects are marked successful if funding target is reached
• ♻️ Refunds are available if target isn’t met
• 📤 Project owners can request withdrawals
• ✅ Contributors vote on withdrawal requests (needs 50%+ votes)

⸻

🛠️ Tech Stack
• Solidity (Smart contracts)
• Hardhat (Local blockchain environment)
• JavaScript / Next (Frontend)
• Metamask (Wallet integration)

⸻

📂 Project Structure

CrowdFundingDapp/
├── contracts/
│ ├── Crowdfunding.sol
│ └── Project.sol
├──client/
├── components/
├── pages/
├── redux/
├── styles/
├── scripts/
│ └── deploy.js
├── test/
├── hardhat.config.js
├── .gitignore
└── README.md

⸻

📜 Smart Contracts Overview

Crowdfunding.sol
• Deploys new Project contracts
• Returns all created projects
• Allows contributions to a specific project

Project.sol
• Handles core project logic
• Accepts ETH contributions
• Marks project as Successful or Expired
• Allows refunds or fund withdrawals with voting

⸻

🥺 Understanding Key Files

scripts/deploy.js
• Uses Hardhat Runtime Environment to deploy Crowdfunding contract on Localhost
• Logs the contract address once deployed

Crowdfunding.sol
• Deploys Project contracts for each campaign
• Maintains an array of all created projects
• Handles contribution logic and event logging

Project.sol
• Handles contribution logic, deadlines, refund logic
• Tracks withdraw requests with voting mechanism
• Contains modifiers for role/access control

hardhat.config.js
• Contains Hardhat configuration, including custom network settings (e.g., localhost)

⸻

✨ How to Use 1. Clone repo: git clone https://github.com/tushal-pethani/crowdfunding-dapp.git 2. Install dependencies:
├──client/ npm install
├── npm install

    3.	Compile contracts:
            ├── npx hardhat compile

    4.	Start a local node:
            ├── npx hardhat node

    5.	Deploy contracts:
            ├── npx hardhat run scripts/deploy.js --network localhost
            Copy the deployed contract address

    6. paste the deployed contract address in client/redux/interactions.js on line 13.

    7. 🔗 Demo Videos
    •	🎥 [How to connect with metamask?](https://drive.google.com/file/d/1j0m6nhn6WtNkClyJEw0fO05HdvDdQlJp/view?usp=sharing)
    •	🎥 [Watch how to create your own test tokens](https://drive.google.com/file/d/1Fqv_H1mggGXF0XOQt5P7re_DcMSjnSSd/view?usp=sharing)

    7.	Interact with deployed contracts (via frontend or Hardhat console)

⸻

🔐 Security Note

Do NOT upload private keys or .env files.
It is safe to upload the deployed contract address — it is needed by frontend apps and users to interact with your contract.

⸻

👌 .gitignore

node_modules/
.env
artifacts/
cache/
debug.log
coverage/
typechain/

⸻

📄 License

MIT License — feel free to fork and build your own version!

⸻

🙌 Contributions

Pull requests are welcome. For major changes, open an issue first to discuss what you’d like to change.
