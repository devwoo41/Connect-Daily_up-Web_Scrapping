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

#### TCP

- 우리의 컴퓨터는 전송계층 (Transport Layer) 에서 사고를 해야한다. 

- 컴퓨터 네트워킹에서 인터넷 소켓, 또는 네트워크 소켓은 인터넷 프로토콜을 기반으로 한 인터넷 등의 컴퓨터 네트워킹에서 양방향 커뮤니케이션의 끝점을 의미한다.

- 포트는 애플리케이션에 대응되거나 프로세스에 대응되는 소프트웨어 커뮤니케이션의 말단이고, 한 서버에 여러 네트워크 애플리케이션이 존재할 수 있게 해준다.

- 파이썬에서는 소켓을 굉장히 쉽게 만들 수 있는데
```
<예시>
import socket
mysock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
mysock.connect( ('data.pr4e.org', 80) )
===========
먼저 socket 모듈을 import하고,

인터넷에 연결되는 소켓을 연속된 문자의 흐름인 스트림 방식으로 만들어준다.

그리고 그 소켓에 data.pr4e.org라는 호스트에 80이라는 포트로 연결을 한다.
```

#### 애플리케이션 프로토콜

- 애플리케이션 레벨에서 소켓을 만들어달라는 요청을 하고 지정된 포트로 소통을 하게끔 소켓을 만든다. 

- 애플리케이션 프로토콜에서 소켓이 어떤것을 주고받을지를 결정한다. 

#### HTTP(HyperText Transfer Protocol)

- 인터넷, 애플리케이션 레이어에서 많이 사용되는데 HTML, 이미지, 문서등을 가져오고 문서외에도 다양한 데이터에도 확장하여 사용 가능하다.

```
http://www.dr-chuck.com/page1.htm
프로토콜     호스트         문서
```
#### 인터넷표준

- 모든 인터넷 프로토콜 기준은 한 기관에 의해 개발되었고, 이 기준과 기관은 IETF(Internet Engineering Task Force) 라고 불린다.

#### ASCII & UTF-8

- 아스키코드의 한계를 극복하기 위해 나온 Unicode 중 UTF-8 인코딩 방식이 가장 실용적으로 추천되는 방식이다.

- 파이썬3에서 모든 문자열은 유니코드이다. 그래서 파일에서 데이터를 가져와 파이썬에서 작업하는 경우 거의 대부분 그냥 작동한다. 그러나 소켓을 통해 네트워크로 데이터를 전송하거나 DB와 연결하는 경우 데이터를 인코딩/디코딩 해야한다.

#### 파이썬 문자열

- 네트워크 소켓 등 외부 자원과 통신하는 경우, 문자열이 아니라 Byte 형식을 사용해야 한다. 따라서 파이썬 3에서는 문자열을 Byte로 인코딩해야할 필요가 있다.

- 외부에서 데이터를 가져오는 경우, 해당 문자셋에 대하여 디코딩을 해야 파이썬3에서 정상적인 문자열로 사용할 수 있다.
```
String    ---> encode() ---> Bytes(UTF-8) ---> send() ---> Socket
```




**REFERENCE**
```
All the Sources and References are 
From.
- Naver-connect Daily-up Web-scrapping with Python
- PY4E
```