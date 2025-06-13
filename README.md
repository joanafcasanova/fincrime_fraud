## Data
1. transactions.csv
	- all transactions conducted by users
	- **created_date**
		when the user made the transaction in UTC
	- **type**
		CARD_PAYMENT - making a payment with a Revolut card
		TRANSFER - sending money externally to a bank account
		TOPUP - receiving money from externally into a Revolut account
		EXCHANGE – explicitly buying one currency for another
		ATM - withdrawing money from an ATM
		FEE – paying for one of the paid plans, device insurance or another service
	- **state**
		COMPLETED - the transaction was completed and the user's balance was changed
		DECLINED/FAILED - the transaction was declined for some reason, for example, due to insufficient balance
		REVERTED - the transaction fully went through yet was rolled back later, so does not count towards user's balance – here is used to verify a new top-up source
	- **amount_gbp**
		transaction amount in GBP – for example, 5.10 is 5 pounds 10 pence
	- **currency**
		the original currency in which the money comes in or is sent out, for exchanges it's the currency being bought

3. users.csv
	- information about the users
	- **created_date**
		when a user signed up in UTC
	- **country**
		country is based on the address a user specifies at registration

3. fraudsters.csv
	- **user_id**
		ID if a user identified as a fraudster for the purpose of this task