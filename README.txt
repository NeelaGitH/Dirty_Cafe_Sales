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
	
	II) If Price is empty, we will use Total Spent/Quantity.
	III) If that errors, we will simply drop the rows.

Formula: 
= 