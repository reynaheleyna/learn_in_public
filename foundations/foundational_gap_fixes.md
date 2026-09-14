# Foundational Gap Fixes 

As a self-taught developer over the years, I noticed some gaps that needed filling out or concepts that need to be reviewed to tighten mastery and craftmanship. I built a workbook for 52 weeks starting September 14, 2026 to help me get up to speed with my own knowledge gaps coming from a diagnostic. The first parts are refreshers to help me tighten my mastery further. 

## 09/14/2026 Day 1 - Statements and Non-Statements 
- Statements are verifiable expressions that either have a value of True or False. 
- Expressions usually require more input to be able to turn into a verifiable statement. Ex: x > 5 on its own won't fly, it will need a value for x to evaluate if it's true or not. 
- For expressions, criteria is usually defined to be able to get truth value as a whole. 
- Python as a programming language has specific behavior when it comes to evaluating Boolean expressions unique to it compared to other programming languages. 

References: 
- https://ocw.mit.edu/courses/6-1200j-mathematics-for-computer-science-spring-2024/resources/mit6_1200j_s24_lec01_pdf/
- https://docs.python.org/3.12/tutorial/datastructures.html
- https://docs.python.org/3/reference/expressions.html 

## 09/15/2026 Day 2 - Truth Values and Negation 
- De Morgan: not (P and Q) is equivalent to (not P) or (not Q); not(P or Q) is equivalent to (not P) and (not Q)
- Neither is not a or not b

Exercises: 
Quick Retrieval: 
1. and requires both expressions to be true
2. or requires at least one expression to be true
3. not will negate or reverse the value, will become false if true and vice versa. 
4. = is assignment to a variable of a value and == denotes equality

Truth Tables: 
P and Q: True, False, False, False 
P or Q: True, True, True, False
not P: False, True 

```
Given:
is_logged_in = True
is_admin = False
has_paid = True
is_banned = False
```

5. True
6. True
7. True
8. False
9. True
10. True
11. not both_banned OR not is_suspended
12. not is_admin and not is_moderator
13. payment_success and stock_available
14. if is_banned = True or user_login = False (is_banned or not is_logged_in)

2nd Challenge: 
1. Equivalent Yes
2. Equivalent Yes
3. Not Equivalent No

References: 
- Chapter 1 - https://courses.csail.mit.edu/6.042/spring18/mcs.pdf 


## 09/16/2026 AND / Conjunction


