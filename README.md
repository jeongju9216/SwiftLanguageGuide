# Swift Language Guide
Swift 개념 정리를 위해 공식 문서 읽기 & 번역을 진행합니다.  
완벽한 번역보다는 한 줄 한 줄 읽는 것에 의의를 두었습니다.

번역 내용은 블로그에 업로드 했으며  
새로 배운 내용만 아래에 한 번 더 정리하였습니다.
<br/><br/>

## Swift 소개
(1) https://jeong9216.tistory.com/171  
(2) https://jeong9216.tistory.com/172
<br/><br/>

## 기본 연산자 (Basic Operators)
https://jeong9216.tistory.com/175

#### 새로 배운 점
- Swift가 C++로 이루어진 만큼 C와 연산자가 유사한 부분이 많다는 점
- 튜플의 연산
<br/><br/>

## 문자열과 문자 (Strings and Characters)
https://jeong9216.tistory.com/177

#### 새로 배운 점
- Swift의 String과 Character 타입은 유니코드 호환으로 텍스트 처리를 빠르게 하였다는 점
- Multiline String 관련 문법
- String의 isEmpty가 Property라는 점
- Extended Grapheme Clusters의 문법
    - 여러 개의 문자를 합쳐 하나의 그래픽으로 나타낸다는 점
    - 똑같이 보이는 문자라도 다른 양의 메모리가 필요할 수 있다는 점
- SubString은 문자열을 참조하는 구조라는 점
<br/><br/>

## 콜렉션 타입 (Collection Types)
https://jeong9216.tistory.com/184

#### 새로 배운 점
- Swift가 C++로 이루어진 만큼 C와 연산자가 유사한 부분이 많다는 점
- 튜플의 연산
<br/><br/>

## 제어 흐름 (Control Flow)
https://jeong9216.tistory.com/187

#### 새로 배운 점
- Dictionary로 for-in 루프를 쓸 때 순서가 보장이 안 된다는 점
- for-in에서 임시 값이 상수로 선언된다는 점
- switch에서 실행된 부분을 선택하는 절차를 switching이라고 한다는 점
- switch에서 튜플로 case를 넣을 수 있다는 점
- switch에서 값 바인딩이 가능하다는 점
- switch에서 값 바인딩을 포함한 혼합 케이스에 대한 내용
- fallthrough 키워드는 switch 케이스 실행을 위한 케이스 조건을 확인하지 않는다는 점 -> 다시 조건을 체크하고 만족하지 않으면 default로 보냄
- Labeled Statements에 대한 내용
- 버전 체크를 마이너 버전으로도 할 수 있다는 점
<br/><br/>

## 함수 (Functions)
https://jeong9216.tistory.com/188

#### 새로 배운 점
- 다른 함수 내에 함수를 정의할 수 있다는 점
- Void가 빈 튜플이라는 점
- 반환되는 튜플의 옵셔널을 튜플 전체를 옵셔널로 감싸서 표현한다는 점
- 반환값이 있는 한 줄로 된 함수는 return을 생략해도 된다는 점
- 가변 파라미터가 배열(array)로 사용 가능하다는 점
- in-out 파라미터는 기본값 설정이 안 된다는 점
<br/><br/>

## 클로저 (Closures)
https://jeong9216.tistory.com/190  

#### 새로 배운 점
- 전역 함수와 중첩 함수가 클로저라는 사실
- sorted 메서드가 클로저를 기반으로 동작된다는 사실
- 클로저의 인자, 반환값 생략할 수 있는 이유가 Swift의 타입 유추라는 점
    - 생략 가능하다는 것은 알고 있었지만 이번 포스팅을 통해 이유를 알게 되었다.
- ">" 연산자 메서드에 문자열별 구현이 되어 있어 sorted()에 클로저 대신 쓸 수 있다는 점
- 클로저는 참조 타입이라는 점
- 값이 캡처가 되면 클로저와 인스턴스 사이에 강한 참조 사이클이 생성된다는 점
- 캡처로 생성된 강한 참조 사이클을 캡처 목록을 사용하여 관리한다는 점
- 이스케이프 클로저에 대한 내용
- 자동 클로저에 대한 내용
<br/><br/>

## 열거형 (Enumerations)
https://jeong9216.tistory.com/192

#### 새로 배운 점
- 열거형 타입은 ‘복수형 (plural) 보단 단수형 (singular)’ 이름을 부여해야 명확하다는 점
- CaseIterable를 채택함으로서 모든 케이스 집합체를 가질 수 있다는 점
- Associated Values에 대한 내용
- case 이름 앞에 var 나 let annotation을 하나만 적어도 된다는 점
- 원시 값으로 문자열을 사용할 땐 그 case 이름에 있는 문장이 각 case 의 암시적인 값이 된다는 점
- 열거형 initializer는 nil을 return할 수 있는 옵셔널형이라는 점
- 재귀 열거형(Recursive Enumerations)에 대한 내용
<br/><br/>

## 구조체와 클래스 (Structures and Classes)
https://jeong9216.tistory.com/216

#### 새로 배운 점
- 구조체 및 클래스를 인터페이스 파일과 구현 파일로 분리하지 않는 것이 Swift만의 특징이라는 사실
- object라는 단어가 클래스 인스턴스만을 지칭한다는 사실
- struct를 더 많이 사용하는 이유가 클래스의 추가적인 기능때문이라는 점
- 구조체나 클래스에서 UpperCamelCase, lowerCamelCase를 맞추는 행위가 표준 스위프트 타입과 일치하려고 하는 것이라는 점
- 콜렉션은 복사 성능 비용을 감소시키려고 최적화 한다는 사실
    - 바로 복사하지 않고 저장되는 메모리를 공유하고 있다가 복사본 중 하나가 수정되면 수정 직전에 요소가 복사된다.
    - 클래스는 참조 타입이므로 복사해서 사용할 경우 복사본 데이터에 주의하며 코딩해야 한다는 점
- 포인터 참조를 나타내기 위해 별표(*)를 쓸 필요가 없다는 사실
- 포인터와 직접 상호 작용해야 하는 경우 표준 라이브러리가 포인터와 버퍼 타입을 제공한다는 점
<br/><br/>

## Properties (속성)
https://jeong9216.tistory.com/319

#### 새로 배운 점
- lazy 속성은 동시에 여러 개의 쓰레드가 접근할 경우 중복으로 초기화가 될 가능성이 있다는 점
- Objective-C와 Swift의 클래스 인스턴스 값과 참조를 저장하는 방법이 다르다는 점 => Swift가 훨씬 단순화 되었다는 점
- computed propety가 실제로는 저장이 안 된고 계산만 한다는 점
- Observers
    - willSet, didSet이 Property Observer라는 카테고리(?)라는 점
    - 옵저버를 가진 속성을 in-out 매개 변수로 함수에 전달하면 willSet, didSet을 항상 호출한다는 점
- property wrapper
    - 중복되는 속성을 재사용 할 수 있다는 점
    - 선언 방법, 활용 방법
    - 인자를 전달할 수 있다는 점
- projected value에 대한 것
- 전역 상수와 변수는 항상 lazily하게 계산된다는 점
- stored type properties는 항상 lazily하게 초기화되며 여러 쓰레드가 접근해도 단 한 번만 초기화되는 것을 보증한다는 점
<br/><br/>

## Methods
https://jeong9216.tistory.com/482

#### 새로 배운 점
- mutating 메서드는 self 프로퍼티에 완전히 새로운 인스턴스를 할당할 수 있다.
- 열거형에서 mutating 메서드는 암시적 self를 같은 열거형의 다른 case로 설정할 수 있다.
- 메서드의 결과를 사용하지 않을 때 @discardableResult를 붙이면 "Result of call to ~~~ is unused" 경고를 표시하지 않는다.
<br/><br/>

## Subscripts
https://jeong9216.tistory.com/483

#### 새로 배운 점
- 클래스, 구조체, 열거형은 서브스크립트(subscripts)를 정의할 수 있다.
- 서브 스크립트를 사용하면 다른 메서드 없이 인덱스를 사용하여 값을 설정하고 검색할 수 있다.
- subscript 키워드로만 서브스크립트를 정의 가능하다.
- 클래스와 구조체는 필요한 만큼의 서브스크립트를 구현할 수 있다.
- 여러 개의 서브스크립트를 정의하는 것을 subscript overloading이라고 한다.
- 사용자 타입에 맞춰 여러 개의 파라미터를 받는 서브스크립트를 정의할 수도 있다.
<br/><br/>

## 초기화(Initialization)
https://jeong9216.tistory.com/486

#### 새로 배운 점
- 상수 프로퍼티는 이니셜라이저 안에서도 초기화할 수 있다.
- 구조체의 기본 이니셜라이저가 Memberwise Initializers라는 이름이라는 것
- designated 이니셜라이저는 해당 클래스가 직접 상속받는 슈퍼클래스의 designated 이니셜라이저를 호출해야 한다.
- convenience 이니셜라이저는 같은 클래스의 다른 이니셜라이저만 호출해야 한다.
- convenience 이니셜라이저는 궁극적으로 designated 이니셜라이저를 호출해야 한다.
- Swift의 컴파일러는 2단계 초기화를 에러 없이 완료하기 위해 4가지 safety-check를 수행한다.
- 서브클래스에서 새로 추가한 모든 프로퍼티에 기본값이 지정되면, 두 가지 규칙이 적용된다.
    - 만약 서브클래스가 어떠한 designated 이니셜라이저도 정의하지 않는다면, 자동으로 슈퍼클래스의 모든 designated 이니셜라이저는 상속된다.
    - 서브클래스가 슈퍼클래스의 모든 designated 이니셜라이저를 구현한 경우(또는 1번 규칙을 만족한 경우), 슈퍼클래스의 모든 convenience 이니셜라이저는 상속된다.
- 클래스, 구조체, 열거형에서 실패할 수 있는 초기화를 정의할 수 있다.
- raw 값을 가지는 열거형은 자동으로 failable initializer, init?(rawValue:)를 생성한다.
- 클래스의 서브 클래스가 해당 이니셜라이저를 필수로 구현하도록 하려면 required 수식어를 클래스 이니셜라이저 앞에 붙여줍니다.
- 프로퍼티를 초기화할 때 클로저를 사용한다면, 인스턴스의 다른 프로퍼티들은 클로저가 수행되는 시점에서 초기화가 완료된 것이 아닙니다.
<br/><br/>

## 인스턴스 해제(Deinitialization)
https://jeong9216.tistory.com/487

#### 새로 배운 점
- 슈퍼 클래스의 소멸자는 슈퍼클래스의 서브클래스에 의해 상속되고, 슈퍼클래스의 소멸자는 자동으로 서브클래스의 소멸자의 끝에 호출됩니다.
<br/><br/>

## 동시성(Concurrency)
https://jeong9216.tistory.com/497

#### 새로 배운 점
- 동시성이 필요한 코드에서 Swift 언어 수준에서 제공하는 동시성을 사용하면 Swift가 컴파일 타임에 문제를 잡는데 도움을 줄 수 있습니다.
- Swift의 동시성 모델은 Thread 위에서 구축되었지만, 직접 상호작용 하지는 않습니다.
- 비동기 메서드 내부에서 실행 흐름은 오직 다른 비동기 메서드를 호출할 때만 일시 정지되는데, 일시중지는 암시적이거나 우선적이지 않기 때문에 가능한 모든 일시중지 지점은 await로 표시됩니다.
- await 키워드가 사용된 코드는 실행을 일시 중지할 수 있어야 하기 때문에, 프로그램의 특정 장소에서만 비동기 함수나 메서드를 호출할 수 있습니다.
    - 비동기 함수, 메서드, 프로퍼티의 본문에 있는 코드
    - @main으로 표시된 구조체, 클래스, 열거형의 static main() 메서드에 있는 코드
    - Unstructured Concurrency에서 볼 수 있듯이 detached child task에 있는 코드
- 비동기 함수를 호출해 주변 코드와 병렬적으로 실행되도록 하려면, 상수를 정의할 때 let 앞에 async를 작성한 다음 상수를 사용할 때마다 await를 작성하면 됩니다.
- 두 접근법의 차이점에 대해 고민하고, 적절하게 사용할 수 있는 방법은 다음과 같습니다.
    - 다음 줄의 코드가 해당 함수의 결과에 따라 달라지는 경우, await를 사용해 비동기 함수를 호출하세요. => 순차 수행
    - 다음 코드에서 결과가 필요하지 않을 때, async-let을 사용해 비동기 함수를 호출하세요. => 병렬 수행
    - await와 async-let 모두 일시 중지된 동안 다른 코드를 실행할 수 있게 합니다.
    - 두 경우 await를 사용해 모든 일시중지 가능 지점을 표시하여 필요한 경우 비동기 함수가 반환될 때까지 실행이 일시 중지됨을 의미합니다.
- Task는 프로그램의 일부로 비동기로 실행될 수 있는 작업의 단위입니다.
- 모든 비동기 코드는 여러 task의 일부로 실행됩니다.
- 이전 단원에서 설명한 async-let 구문은 child task를 생성합니다.
- 또한 task group을 생성하고 해당 그룹에 child tasks를 추가하여 우선순위 및 해제를 보다 세부적으로 제어할 수 있으며, 동적으로 여러 task를 생성할 수 있습니다.
- 현재 actor에서 실행되는 구조화되지 않은 task를 생성하려면 Task.init(priority:operation:) 초기화 구문을 호출해야 합니다.
- 현재 actor의 일부가 아닌 구조화되지 않은 task를 생성하려면 Task.detached(priority:operation:) 클래스 메서드를 호출합니다.
- Actors와 Sendable에 관한 내용
<br/><br/>

## 타입 캐스팅(Type Casting)
https://jeong9216.tistory.com/499

#### 새로 배운 점
- 클래스와 서브클래스의 계층 구조가 있는 타입 캐스팅을 사용하여 특정 클래스 인스턴스의 타입을 확인하고 그 인스턴스를 같은 계층에 있는 다른 클래스로 캐스팅할 수 있습니다.
- Any 또는 AnyObject 타입에서 알고 있는 상수나 변수의 특정 타입을 찾으려면, switch문에서 is 또는 as 패턴을 사용할 수 있습니다.
<br/><br/>

## Automatic Reference Counting (ARC)
https://jeong9216.tistory.com/454

#### 새로 배운 점
- 참조 카운트는 클래스의 인스턴스에서만 적용된다.
- ARC는 메모리 해제 뿐만 아니라 메모리 할당, 추적의 역할도 한다.
- 약한 참조는 다른 인스턴스의 수명이 더 짧을 때 사용해야 한다.
- 미소유 참조에 대한 개념
- 미소유 참조는 다른 인스턴스의 수명이 같거나 더 길 때 사용해야 한다.
- 모두 nil이 허용되면 weak를 이용해 강한 순환 참조를 방지한다.
- nil이 허용되는 하나의 속성과 nil이 될 수 없는 다른 속성일 때는 unowned를 이용해 강한 순환 참조를 방지한다.
- 캡처 리스트에 대한 전반적인 내용
<br/><br/>
