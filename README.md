Wallet Microservice System
Overview
The Wallet Microservice System is designed to provide a secure and efficient platform for managing digital wallets, catering specifically to users aged 6–17 who are residents of the UK. This system allows users to view their Know Your Customer (KYC) details, account information, and wallet balance, while also enabling them to initiate transactions for various products and services. The system incorporates features such as trusted payee setup, gambling control, and restrictions on payments for certain items like cigarettes, cocaine, and alcohol.

Microservices
1. Wallet Service
Provides functionalities related to managing user wallets, including viewing KYC details, account information, and wallet balance.
Implements trusted payee setup and controls for restricted payments.
Ensures validation of wallet balance before processing transactions.
Validates the currency for trading purposes.
Facilitates communication with the Payment Service for transaction processing.
Initiates referral to Guardian/Parent for transactions requiring approval.
Collects wallet fees and credits merchant accounts after successful payment processing.
2. Payment Service
Handles the processing of transactions initiated by the Wallet Service.
Deducts transaction amounts from user wallets and credits merchant accounts.
Maintains an updated transaction ledger.
Sends notifications to merchants upon successful payment processing.
Manages settlement of actual funds to merchants.
3. Audit Service
Captures audit information throughout the transaction lifecycle.
Ensures transparency and accountability in system operations.
Facilitates monitoring and analysis of system activities.
4. Notification Service
Sends notifications to users regarding transaction status updates.
Provides real-time information to users to keep them informed about their transactions.
5. Transaction Failure Service
Handles the failure of transactions and rollsback to compensate the initiator.

Initiation Flow
User Interaction: User initiates a transaction by providing product details, cost, currency, and merchant information.
Validation: Wallet Service validates the transaction by checking wallet balance, currency validity, and any restrictions.
Approval (if needed): Referral to Guardian/Parent for approval in case of certain transactions.
Transaction Processing: Payment Service processes the transaction by deducting the amount from the user's wallet, crediting the merchant's account, and updating the transaction ledger.
Notification: Notification Service sends status updates to the user and notifications to the merchant upon successful processing.
Fee Collection: Wallet Service collects wallet fees and credits the merchant's account after deduction.

Transaction Management
Ensures reliability and integrity of transactions.
Compensates for any failures appropriately.
Captures audit information at every stage for traceability and accountability.
Provides accurate status notifications to users throughout the transaction lifecycle.
Usage
To deploy and use the Wallet Microservice System, follow the instructions provided in each microservice's README.md file.

Contributors
Sourabh Savagunji
Gaurav Gupta
