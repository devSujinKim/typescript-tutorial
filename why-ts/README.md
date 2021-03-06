# Why TypeScript?

## 타입스크립트란?
> 공식 홈페이지에 따르면 “Typescript는 정적 유형 정의를 추가하여 Javascript를 기반으로 하는  
> 오픈 소스라고 말하고 있으며 Type을 추가함으로써 코드가 올바르게 작동하는지 확인할 수 있다” 라고 말하고 있다.  
> 
> 타입스크립트는 자바스크립트에 타입을 부여한 언어이다.  
> 자바스크립트의 확장된 언어라고 볼 수 있다.

## 타입스크립트를 왜 사용해야 하는가?
에러의 사전 방지
```javascript
function sum(a, b) {
  return a + b;
}
sum('10', '20'); // 1020
```
위 함수는 숫자 2개를 a, b에 인자로 전달받아 그 합계를 리턴하고자 한다.  
하지만 코드상으로는 어떤 타입의 인수를 전달하여야 하는지, 어떤 타입의 반환 값을 리턴해야 하는지 명확하지 않다.

아래 ts로 작성된 코드를 보자.
```javascript
function sum(a: number, b: number) {
  return a + b;
}
sum('10', '20'); // Error
```
a, b 인자는 number 타입이라고 명시되어 있다.  
따라서 "'10'은 number에 할당될 수 없습니다." 라는 오류를 확인할 수 있다.

✏️ `TypeScript는 정적 타입을 지원하므로 컴파일 단계에서 오류를 확인할 수 있는 장점이 생긴다.`  
✏️ `Typescript는 코드를 보다 읽기 쉽게 만든다.`  
✏️ `Typescript는 개발자의 실수를 줄여준다.`
