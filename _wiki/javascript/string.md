---
layout  : wiki
title   : String()과 new String()의 차이
date    : 2023-01-11 18:14:00 +0900
updated : 2023-01-11 18:14:00 +0900
author  : 김현지, 우종혁
tag     :
toc     : true
public  : true
parent  : javascript
latex   : false
---
* TOC
{:toc}

String 생성자는 새로운 String 객체를 만듭니다. 함수로 호출하게 되면 기본 문자열로 유형을 변환시킵니다.
자바스크립트는 String 오브젝트와 원형의 문자열을 다르게 취급합니다.
문자열 리터럴과 생성자 없이 String을 호출하여 반환된 문자열은 원형 문자열(primitive strings) 입니다.
자바스크립트는 자동적으로 원형을 String 오브젝트로 변환하기 때문에, String 오브젝트 메서드를 사용하여 원형 문자열을 생성할 수 있습니다.
프로퍼티 조회 또는 원형의 문자열 호출이 발생하면, 자바스크립트는 자동으로 문자열 원형을 감싸고 프로퍼티를 조회하거나 toString()메서드를 호출합니다.
String()과 new String()은 서로 다른 결과를 생성합니다.
String()은 문자열을 생성하지만 객체 생성 프로세스인 new를 사용하면 String 유형의 인스턴스(객체)를 생성합니다.

```jsx
let s_prim = String('foo');
let s_obj = new String(s_prim);

console.log(typeof s_prim); // string
console.log(typeof s_obj); // object
s_prime instanceof String; // is false
s_obj instanceof String; // is true
```
