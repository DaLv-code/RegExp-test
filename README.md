# 정규표현식(RegExp)


## 정규표현식 생성

```js
// 생성자
new RegExp('표현','옵션')
new RegExp('[a-z]','gi')

// 리터럴
/표현/옵션
/[a-z]/gi
```

## 문자열 예시
```js
const str = `
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum
`
```

## 메소드
메소드|문법|설명
--|--|--
test | `정규식.text(문자열)`|일치 여부(Boolean) 반환
match | `문자열.match(정규식)`|일치하는 문자의 배열(Array) 반환
replace | `문자열.replace(정규식,대체문자)`|일치하는 문자를 대체

## 플래그(옵션)
플래그|설명
--|--
g| 모든 문자 일치(global)
i| 영어 대소문자를 구분하지 않고 일치(ignore case)
m| 여러 줄 일치(multi line)

## 패턴(표현)
패턴|설명
--|--
^ab | 줄(Line) 시작 부분의 ab와 일치
ab$ | 줄(Line) 끝에 있는 ab와 일치
. | 임의의 한 문자와 일치
a\|b | a또는 b와 일치
a..b? | b가 없거나 b와 일치
{3} | 3개 연속 일치
{3,} | 3개 이상 연속 일치
{3,5} | 3개이상 5개 이하 연속 일치
[abc] | a 또는 b 또는 c
[a-z] | a부터 z 사이의 문자 구간에 일치
[A-Z] | A부터 Z 사이의 문자 구간에 일치
[0-9] | 0부터 9사이의 문자 구간에 일치
[가-힣] | '가'부터 '힣'까지 문자 구간에 일치
\w | 63개 문자(Word, 대소영문52개 + 숫자10개 + _)에 일치
\b | 63개 문자(Word, 대소영문52개 + 숫자10개 + _)를 제외한 문자 경계(Boundary)
\d | 숫자(digit)에 일치
\s | 공백(Space,Tab 등)에 일치
(?=) | 앞쪽 일치(Lookahaed)
(?<=) | 뒤쪽 일치 (Lookbehind)