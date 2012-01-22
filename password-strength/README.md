Password Strength Check
=======================

Problem
--------
As a payment processor security is something that is important to us.  One aspect of security is ensuring that users set strong passwords.  We’d like you to write a routine that verifies password strength using the following rules:

1.	All passwords must be at least 8 characters in length
2.	All passwords must contain at least one capital letter
3.	All passwords must contain at least 2 digits
4.	All passwords must contain a punctuation character (non Alpha-Numeric)

boolean verifyPasswordStrength(String password)


Sample Test Cases
-----------------

Case 1:

Input: foobar 
Output: false

Case 2:

Input: F00bar_ru1eZ 
Output: true


Extra Credit
------------

Create a utility for suggesting a password in cases where the strength is not sufficient.  You should utilize some element of what the user entered for the suggested new password
