I got this data: https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training from Kaggle for practicing data cleaning.

FOLLOWING ARE THE STRATEGIES USED TO FILL UP THE ERROR/NULL/UNKNOWN DATA.
1. Fix Item Column:
- To fill the unknown data, we will use the following strategies:
	I) Use Price Column: 
		Item	Price($)
		Coffee	2
		Tea	1.5
		Sandwich	4
		Salad	5
		Cake	3
		Cookie	1
		Smoothie	4
		Juice	3
	Note: Since for $4 and $3 we have two items, we will use the most common item bought for that price from that store.
	For $3 - Juice
	For $4 - Sandwich
	
	II) If Price is empty, we will use Total Spent/Quantity to first find the price, then fill the item as above.
	III) If that errors, we will simply drop the rows.

2. Fix the Price Column:
- Since we have already fixed the item column, we will only use only the item column to fill up the price column:
		Item	Price($)
		Coffee	2
		Tea	1.5
		Sandwich	4
		Salad	5
		Cake	3
		Cookie	1
		Smoothie	4
		Juice	3

3. Fix the Quantity Column:
- We will use Total Spent/Price. If Total Spent is not available, we will ASSUME the quantity is 1.
Note: Price(Modified Column) will always be available because we dropped the erroneous data.

4. Fix the Total Spent:
- Now we have good data for Price and Quantity, so we used
	Total Spent = Price * Quantity

5. Fix the Payment Method and Location:
We used the mode of the columns to fill up the unknown.
	Mode of Payment Method = Digital Wallet
	Mode of Location = Takeaway

6. Fix the Transaction Date Column:
We used mode for this too, because the rows were randomly added, so we couldn't find a relevant connection of unknown dates with its nearby rows.
Mode =  06-02-2023

