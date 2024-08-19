# sql_sba_prep

### Problem Statement:
Write a SQL query to find the average sale price of properties that have been **successfully sold** by each agent, rounded to the nearest dollar. Display the agent's full name and the average sale price. Only include agents who have completed at least one sale.

### Database Schema:
You are working with the following tables:

- **Agents**
  - `AgentID` (Primary Key)
  - `FirstName`
  - `LastName`
  - `Email`
  - `PhoneNumber`

- **Transactions**
  - `TransactionID` (Primary Key)
  - `PropertyID`
  - `ClientID`
  - `AgentID`
  - `SalePrice`
  - `SaleDate`
  - `StatusID` (Foreign Key referencing `PropertyStatus.StatusID`)

- **PropertyStatus**
  - `StatusID` (Primary Key)
  - `StatusName` (e.g., 'Available', 'Under Contract', 'Sold')

### Additional Details:
- You need to join the `Transactions` table with the `Agents` table to get the agent’s full name.
- Join the `PropertyStatus` table to filter out only those transactions where the status is `'Sold'`.
- Group the results by `AgentID` to ensure that each agent's data is aggregated correctly.
