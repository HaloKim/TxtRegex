# Txt Regex
[TxtRegex]https://pypi.org/project/TxtRegex/

파이썬의 정규표현식이 어려워 자주사용하는 기능만 구현해올려놨습니다.

---
## Version
	python >= 3.0
  
## Install
	pip install TxtRegex
  
## 기능
- 이메일(Email)
- URL
- 핸드폰 번호(Phone Number)
- 계좌(Account)

# How to use ?
### CODE
	from TxtRegex import regex

	txt = '''
	좋은 아침입니다.
	제 이메일은 dev7halo@gmail.com 입니다
	전화번호는 010-1234-1234, 031-123-4567 입니다.
	계좌번호는 신한 110-444-261900, 국민 293802-01-205141 입니다.
	블로그 주소는 https://github.com/HaloKim 입니다.
	'''

	print(regex.convert("email", txt, ""),"\n")
	print("\n".join(regex.convert("url", txt, "")),"\n")
	print("\n".join(regex.convert("number", txt, "")))
### OUTPUT
	['좋은 아침입니다.', '제 이메일은  입니다', '전화번호는 010-1234-1234, 031-123-4567 입니다.', '계좌번호는 신한 110-444-261900, 국민 293802-01-205141 입니다.', '블로그 주소는 https://github.com/HaloKim 입니다.'] 

	좋은 아침입니다.
	제 이메일은 dev7halo@gmail.com 입니다
	전화번호는 010-1234-1234, 031-123-4567 입니다.
	계좌번호는 신한 110-444-261900, 국민 293802-01-205141 입니다.
	블로그 주소는  입니다. 

	좋은 아침입니다.
	제 이메일은 dev7halo@gmail.com 입니다
	전화번호는 ,  입니다.
	계좌번호는 신한 , 국민  입니다.
	블로그 주소는 https://github.com/HaloKim 입니다.
	
# Future work
- Phone 번호와 계좌번호 분리 작업
