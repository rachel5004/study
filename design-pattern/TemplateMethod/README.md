# 템플릿 메서드란

`템플릿 메서드`란 부모 클래스에서 알고리즘의 골격을 정의하지만 해당 알고리즘의 구조를 변경하지 않고  
자식 클래스들이 알고리즘의 특정 단계들을 오버라이드(재정의)할수 있도록 하는 디자인 패턴
![스크린샷 2022-11-13 오후 2 26 12](https://user-images.githubusercontent.com/37957608/201507270-d60e368c-efb5-42e1-8d57-8ae77817f765.png)

---

# 템플릿 콜백(Template-Callback) 패턴

콜백으로 상속 대신 위임을 사용하는 템플릿 패턴  
상속대신 익명 내부 클래스 또는 람다 표현식을 활용할 수 있다.
![스크린샷 2022-11-13 오후 2 26 52](https://user-images.githubusercontent.com/37957608/201507287-128bc630-d307-4723-a8c5-103fab12ff1c.png)

전략 패턴처럼 어떤 전략을 제공해주는 거라 볼수 있다.
다른 점은 여러개 메소드를 가지고 있을수 있지만 콜백 패턴 같은 경우는 하나만 가능.
좋은 점은 상속을 사용하지 않아도 된다.

## 또한 이 패턴은 스프링에서 많이 쓰이고 있다.

# 장단점

- 장점
  - 템플릿 코드를 재사용하고 중복 코드를 줄일 수 있다.
  - 템플릿 코드를 변경하지 않고 상속을 받아서 구체적인 알고리즘만 변경할 수 있다.
- 단점
  - 리스코프 치환 원칙을 위반할 수도 있다.
  - 알고리즘 구조가 복잡할수록 템플릿을 유지하기 어려워진다.