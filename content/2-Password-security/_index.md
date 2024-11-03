---
title : "Password security"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---
### Passwords

Passwords are one of the most basic yet critical components of digital security. However, weak passwords expose accounts to significant risk.

There are common passwords that people use:

1. 123456
2. admin
3. 12345678
4. 123456789
5. 1234
6. 12345
7. password
8. 123
9. Aa123456
10. 1234567890

If you have one of the passwords above, most likely, millions of people have the same password as you!
Bad guys can also guess most of the heuristics you use to add symbols to your password. Adversaries can use brute-force attacks, using a dictionary of passwords to simply try every possible password. Your password is likely not as secure as you think it is.

A strong password should include:

- At least 12–16 characters
- A mix of uppercase, lowercase letters, numbers, and symbols
- No common phrases or easily guessable patterns

For instance, `G7!klpQr92@wD` is a more secure password. An eight-character password containing letters, numbers, and symbols has approximately **6 quadrillion possible combinations**, making brute-force attacks much harder.

### Password managers

Password managers can be used to create very challenging passwords and remember them for you. The probability of a password secured by a password manager being broken is very, very low.

You’d hope that such password managers are secure. However, if one gains access to your password manager, they would have access to all your passwords. Hence, it’s crucial to recognize that password managers themselves must be well-protected

### Phone security

Many phones are secured by a four-digit code. There are 10,000 possible passwords when using a four-digit code. The most simple form of attack would be to brute-force attempt all possible passwords.

If it takes one guess per second, it will take 10,000 seconds to crack the password.
However, if a programmer creates a program to generate all possible codes, the time required would be minimal. Consider the following code in Python:
```python
from string import digits
from itertools import product

for passcode in product(digits, repeat=4):
    print(passcode)
```
It should be quite disconcerting that the code above could take only a few seconds (at most!) to discover your password.
We could improve our security by switching to a four-letter password. This would result in 7,311,616 possible passwords.
Including uppercase and lowercase characters would create over 78 million possibilities.
Consider how we could modify your code to discover these passwords:
```python
from string import ascii_letters
from itertools import product

for passcode in product(ascii_letters, repeat=4):
    print(passcode)
```
We could even add the ability to look at all possible eight-digit passwords with letters, numbers, and punctuations:
```python
from string import ascii_letters, digits, punctuation
from itertools import product

for passcode in product(ascii_letters + digits + punctuation, repeat=8):
    print(passcode)
```
Expanding to eight characters, including upper and lowercase letters, numbers, and symbols, would result in 6,095,689,385,410,816 possible combinations.

In the digital world, you simply want your password to be better than other peoples’ passwords such that others would be attacked far before you — as you are a much less convenient target.

A downside of using such a long password is the downside of having to remember it.

Accordingly, there are other defenses that could be employed to slow down an attacker. For example, some phone manufacturers lock out those who guess a password incorrectly.
Security is about finding a “sweet spot” between the trade-offs of enhanced security while maintaining convenience.
