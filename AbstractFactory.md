# 추상 팩토리 패턴
추상 팩토리 패턴은 큰 규모의 객체 군을 형성하는 생성 패턴입니다.

## 팩토리 메서드
팩토리 메서드는 객체 생성을 담당하는 클래스를 추상화하여 선언과 구현을 분리한 확장 패턴입니다.

 

팩토리 패턴과 팩토리 메서드 패턴의 차이는 추상화입니다.

팩토리 메서드 패턴과 추상 팩토리 패턴의 차이는 추상화된 그룹을 형성하고 관리하는 것입니다.


팩토리 메서드의 상위 클래스는 추상적 선언입니다. 추상적 선언은 하위 클래스에서 적용되는 인터페이스와 유사합니다.

또한 하위 클래스에 필요한 공통 내용을 포함합니다.

즉, 인터페이스에 따라 하위 클래스에서 오버라이드 되고, 실제 동작하는 메서드의 내용을 구현됩니다.

 

## 그룹
추상 팩토리는 여러 개의 팩토리 메서드를 그룹으로 묶은 것과 유사합니다. 

 

추상화는 다형성을 적용해 여러 개의 하위 클래스를 생성할 수 있습니다.

 

팩토리 메서드는 추상 클래스와 하위 클래스를 1개로만 구성합니다.

 

반면, 추상 팩토리는 다형성을 적극적으로 활용하여 다수의 하위 클래스를 생성하고 관리하는 것이 특징입니다.

 

## 팩토리 그룹
추상 팩토리는 다양한 객체 생성 과정에서 그룹화가 필요할 때 매우 유용한 패턴이며 공장의 개념을 추상화 합니다.

 

즉, 복수의 객체 생성을 담당하는 군집을 관리하는 것입니다.


추상화는 인터페이스를 전달하고 상속을 통해 실제 로직을 하위 클래스에 구현합니다. 

 

즉, 실제 생성되는 로직을 하위클래스에 구현하는데, 이는 실제 동작하는 구현부를 외부로부터 감출 수 있습니다.

 
장점과 단점
장점

1. 큰 변화없이 시스템의 군을 생성하고 변경할 수 있습니다.

2. 코드를 일관적으로 유지하고 실제 구현을 다르게 실행시킬 수 있습니다.

 

단점

1. 새로운 종류의 군을 추가하는 것이 쉽지 않습니다.

2. 새로운 종류를 추가할 때마다 구조를 재설계하는 것은 확장성 부분에서 좋지 않습니다.
