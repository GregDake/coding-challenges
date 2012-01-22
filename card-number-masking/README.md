Credit Card Number Masking
==========================

Problem
--------
As a payment processor security is something that is important to us.  Processing credit card data means never storing an unencrypted card number.  In order to achieve this goal we require a utility to flag any text and identify if this text contains a card number.  This program should mask the card by using a masking character of ‘X’ for all but the last 4 digits of the number.  

Your program should mask anything that looks like a credit card number. If a number like "4111 1111 1111 1111" were accidentally logged as part of an error message, our filter would replace it with "XXXX XXXX XXXX 1111".

A well-formed credit card number can be identified by the following rules for the purpose of this exercise:

-	14-19 digits in length
-	Complies with Luhn check described below 

The Luhn check is a simple checksum algorithm invented by Hans Peter Luhn in 1954.  All valid credit card numbers pass the Luhn check, thereby enabling computer programs to distinguish credit card numbers from random digit sequences.

The Luhn check works like this (You can find a lot more info on the internet if needed)

   1. Starting from the rightmost digit and working left, double every second digit.
   2. If a product has two digits, treat the digits independently.
   3. Sum each individual digit, including the non-doubled digits.
   4. Divide the result by 10.
   5. If the remainder is 0, the number passed the Luhn check.

For example, "5678" passes the Luhn check:

   1. Double every other digit: 10, 6, 14, 8
   2. Sum the individual digits: (1 + 0) + 6 + (1 + 4) + 8 = 20
   3. Divide the result by 10: 20 mod 10 = 0 Pass

"7785" does not:

   1. Double every other digit: 14, 7, 16, 5
   2. Sum the individual digits: (1 + 4) + 7 + (1 + 6) + 5 = 24
   3. Divide the result by 10: 24 mod 10 != 0 Fail


Sample Test Cases
-----------------

Case 1:

  Description:     valid 14-digit #
  Input:           56613959932537
  Expected result: XXXXXXXXXX2537

Case 2:

  Description:     valid 16-digit # with dashes
  Input:   5589-5500-0000-0044        
  Expected result: XXXX-XXXX-XXXX-0044


Case 2:

Description:     invalid 16-digit # - no masking
Input:           4147395993253712
Expected result: 4147395993253712
