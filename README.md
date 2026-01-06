## Regular Expression

### Understanding Regular Expressions
- 기호로 되어 있어 효과적이지만 조금 어렵다.
- 한번 배우면 활용할 곳이 많다.
- 정규식은 그 자체로 하나의 언어이다.
- 특수 문자로 이루어진 언어로 문자만을 사용해서 프로그래밍을 하는 개념이다.
- 축약된 '형식 언어'의 한 종류이다.

```
Python Regular Expression Quick Guide

^        Matches the beginning of a line
$        Matches the end of the line
.        Matches any character
\s       Matches whitespace
\S       Matches any non-whitespace character
*        Repeats a character zero or more times
*?       Repeats a character zero or more times 
         (non-greedy)
+        Repeats a character one or more times
+?       Repeats a character one or more times 
         (non-greedy)
[aeiou]  Matches a single character in the listed set
[^XYZ]   Matches a single character not in the listed set
[a-z0-9] The set of characters can include a range
(        Indicates where string extraction is to start
)        Indicates where string extraction is to end
```

All the Sources and References are 
From.
- Naver-connect Daily-up Web-scrapping with Python
- PY4E