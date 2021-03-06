# 싱글턴 패턴

싱글턴 패턴은 생성 패턴 중 가장 많이 주목받는패턴 중 하나입니다. 자원 공유를 위해 객체 생성 개수를 1개로 제한합니다.

## 객체 생성

객체 생성은 선언된 클래스에 따른 객체를 메모리에 할당하는 동작입니다.

 
시스템 자원이 허락하는 한 무제한으로 객체를 생성할 수 있습니다.

 

객체지향에서 new 키워드로 생성된 객체는 각각 독립된 자원입니다. 서로 다른 메모리 영역을 차지하고 있다는 것을 의미합니다.

 

객체의 상탯값을 공유할 수 없다는 것을 의미합니다.

 

변수는 크게 전역 변수와 로컬 변수로 구분합니다. 변수의 접근 영역 구분을 스코프라고 합니다.. 전역변수는 프로그램 전반에서 접근 가능한 공용 변수로 데이터를 쉽게 공유할 수 있다는 장점이 있습니다.

 

그러나 스코프의 변수 범위를 보다 면밀하게 관리해야 합니다. 잘못하면 사이드 이펙터 부작용으로 오동작이 발생할 수 있습니다.


## 싱글턴
전역 변수처럼 생성한 객체를 공유하려면 하나의 객체만 존재해야 합니다. 

 

싱글턴은 아래와 같은 경우에 유용합니다.

 

- 공유 자원 접근

- 복수의 시스템이 하나의 자원에 접근할 때

- 유일한 객체가 필요할 때

- 값의 캐시가 필요할 때

 

싱글턴을 만드는 경우

 

1. 일단은 생성자를 제한 시켜줍니다.. 접근 속성을 public에서 private로 변경을 하면 접근을 할 수가 없습니다.

 

객체를 만 드는 방법은 new 키워드가 유일합니다.

 

하지만 예외적으로 객체를 복제하여 새로운 객체를 만드는 방법이 있습니다.

 

이때 사용하는 키워드는 clone 입니다. 이 역시 private로 수정을 해줘야 합니다.

 

2. 내부에 선언된 메서드를 호출을 해줌으로써 객체를 생성합니다. 

 

getInstance만 public로 만들어 주면서 객체를 생성할 수 있게 해줍니다.

 

외부에서 정적 메서드를 여러 번 호출하면 매번 다른 객체를 생성하여 반환합니다.

 

따라서 완벽한 싱글턴 패턴은 객체 생성을 외부의 접근 권한만으로 제한할 수 없습니다.

 

이에 어떤 경우라도 1개의 객체만 생성하기 위해서 플라이웨이트 패턴에서 응용되는 참조체를 도입합니다.

 

$Instance 는 참조체입니다..

 

조건문을 통해서 참조체에 저장된 객체를 반환합니다.

 

싱글턴 패턴은 본연의 목적을 해결하기 위해 고유한 처리로직을 가지고 있습니다.

 

또한 중복된 객체 생성을 방지하기 위한 책임을 가지고 있습니다.

 

이에 단일 책임 원칙을 위반합니다... 객체지향의 원칙을 반드시 적용해야 하는 것은 아닙니다. 예외적인 상황과 목적을 

 

위해서 위반하는 경우도 많습니다.

 

## 싱글턴의 확장
일반적으로 잘 사용하지는 않지만 싱글턴 클래스를 상속받을 수 있습니다.

 

싱글턴은 private로 선언되기 때문에 선언된 클래스로 객체를 생성하고 확장할 수 없습니다.

 

Protected 속성으로 변경하면 싱글턴으로 변경된 클래스를 상속받을 수 있습니다.



싱글턴은 패턴 카탈로그에서 4대 패턴에 들어가는 인기 패턴입니다. 그렇지만 올바르게 사용하기 위해서는 숙달된 경험


은 필수입니다..
