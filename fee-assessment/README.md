Fee Assessment Challenge
========================

Problem
-------
Design an algorithm for assessing the fees for a specific financial transaction.  The fees for this transaction will have both a flat rate (for example $0.10) and a percentage component (1.96%).  Fees are calculated based on the transaction amount, which is always in $USD.

Your function must take 3 arguments as follows and return the fee amount:

getFeeAmount(double transactionAmt, double percentFee, double flatFee)

A specific rounding algorithm must be followed for rounding fees to the nearest $0.01.  This rounding algorithm must be used for calculating all fees.  The details of this algorithm are the following:

-	Drop all but 3 digits after the decimal
-	For example if the fee calculated is 1.91223.  This is truncated to become 1.912 (retaining 3 places after the decimal)
-	Once you have dropped all but 3 decimal digits the next step is to employ bankers rounding (round half to even).
-	In the case above you’d then round 1.912 to 1.91 using bankers rounding also called half even rounding.  Google for bankers rounding and you'll get plenty of examples.

You are encouraged to break your code up into separate functions for rounding and truncating.

Sample Test Case
-----------------

Input:
Amount: $35.86
Flat fee: $0.05
Percent fee: 2.45%

Output:
$0.93

Extra Credit
------------
Design your fee assessment routine to handle source currencies that are not in USD.  The transaction amount must first be converted into $USD since all fee's apply to the $USD converted amount.  You can use a fixed currency conversion table to do this task or just make up some rates.  Note that currency conversion is another spot where rounding will apply, amounts should be rounded to an even penny.  Choose the method of rounding that you'd use if this was your business and comment on why you selected this approach.



