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
