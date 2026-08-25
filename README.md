# css 실습
이론 수업과 병행되는 실습 내용을 주로 올립니다.

## day01 
### 1. HTML에 CSS를 적용하는 방법
1. 인라인 스타일
   태그의 style 속성에 직접 작성하는 방식

2. 내부 스타일시트
   <style></style> 안에 작성하는 방식
   style 태그는 head 태그 안에 있어야 한다.
   
3. 외부 스타일시트
   별도의 css파일을 작성하고 HTML 문서에 연결한다.<br/>연결은 link 태그를 이용한다.

### 2. 문법

기본

```
selector {
    attribute : value;
  }
```

주석
```
  /* 주석입니다. */
```

중첩

```
selector{ /* parent */
  attribute: value;
  selector { /* child */
    attribute : value;
    selector { /* descendant  */
      attribute: value;
    }
  }
}
```

#### 2.1 선택자 명시도

### 3. 선택자 

클래스
```
  .class{
    attribute : value;
  }
```
아이디
```
  #id{
    attribute : value;
  }
```

자식
```
  parent > child {
    attribute : value;
  }
```
자손
```
  parent descendant {
    attribute : value;
  }
```

형제 선택

인접 형제 결합자 next-sibling combinator
```
  selector + selector {
    attribute : value;
  }
```

일반 형제 결합자 subsequent-sibling combinator 
```
  selector ~ selector {
    attribute : value;
  }
```

https://github.com/benchel/learn-css/blob/6b207edd762b1da5011f9fd4bf6b5a6d43f57977/day01/selector2.html#L19-L31

https://github.com/benchel/learn-css/blob/6b207edd762b1da5011f9fd4bf6b5a6d43f57977/day01/style/selector2.css#L1-L5

특성 선택자<br/>속성 값으로 조회하여 선택

...로 시작하는 속성값을 갖는 요소 선택
```
selector[attribute^="..."] {
  attribute : value;
}
```

...로 끝나는 속성값을 갖는 요소 선택
```
selector[attribute$="..."] {
  attribute : value;
}
```
...를 포함하는 속성값을 갖는 요소 선택
```
selector[attribute*="..."] {
  attribute : value;
}
```

가상클래스
```
  selector:pseudo-class {
    attribute : value;
  }
```

가상요소
```
  selector::pseudo-element {
    attribute : value;
  }
```
## day02 
### 2. CSS 속성
