
# DealIN Merchant Account Management  

## DealIN Merchant Account Creation

```mermaid
sequenceDiagram
participant Merchant DB
participant AppSync
participant Platform Svces
participant Token Svces
Merchant DB -->> AppSync: createMerchantAccount 
AppSync -->> Platform Svces: createMerchantAccount
Platform Svces -->> Token Svces: createMerchantBlockchainDetails
Token Svces -->> Platform Svces: returnMerchantBlockchainDetails
Platform Svces -->> Merchant DB: returnCreateMerchantAccountResult  
```

## DealIN Merchant Account Update

```mermaid
sequenceDiagram
participant Merchant DB
participant AppSync
participant Platform Svces
participant Token Svces
Merchant DB -->> AppSync: updateMerchantAccount 
AppSync -->> Platform Svces: updateMerchantAccount
Platform Svces -->> Merchant DB: returnUpdateMerchantAccountResult  
```

