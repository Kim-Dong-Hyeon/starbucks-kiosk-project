# Swift 문법 복습 과제 - 키오스크 프로그래밍

💡 **Goal : 키오스크 프로그래밍**

- 지금까지 배운 Swift 문법을 응용해서 **키오스크 프로그래밍** 과제를 완성해 봅시다

📌 **Requirement : 과제에 요구되는 사항이에요.**



- 필수 구현 사항 구현을 목표로 선택 구현 사항도 시도해보시기 바랍니다!
- 우리의 목표는 차례차례 구현해서 키오스크 프로그래밍을 완성하는 것이 목표입니다. 
완성하셨다면 lv4, 5도 도전해보세요!

### 필수 구현 사항

- Lv0
    - 요구사항별로 상세 기능을 생각해요
    - 사용하면서 발생할 수 있는 예외사항들을 생각해요
    - 프로젝트 생성 레퍼런스
        - macOS command line tool로 프로젝트 생성하세요.
        [https://igotit.tistory.com/entry/Xcode-Command-Line-Tool-프로젝트-만들기](https://igotit.tistory.com/entry/Xcode-Command-Line-Tool-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0)
    
    ```text
    [ 필요한 기능 ]
    요구사항1: 메인 메뉴판 화면
    : 메뉴 선택시 상세 메뉴화면으로 이동
    : 잘못된 번호 선택 시 예외처리
    : 프로그램 종료을 위한 번호 정의
    
    요구사항2: ~~~
    요구사항3: ~~~
    요구사항4: ~~~
    ```
    
- Lv1
    - 입력받은 숫자에 따라 다른 로직을 실행하는 코드를 작성해요
    - if나 switch, guard 문을 활용해요
    - 반복문을 이용해서 특정 번호가 입력되면 프로그램을 종료해요
    - readline 함수로 값을 입력받으세요.
        
        ```swift
        // 입력값 받기
        let a = readline()
        
        // 옵셔널, 언래핑 기억하시나요? 강제 언래핑이 장단점과 강제 언래핑이
        // 아니라면 어떻게 적용해보면 좋을까요?
        print(a!)
        ```
        
    
    ```bash
    아래 메뉴판을 보시고 메뉴를 골라 입력해주세요.
    
    [ SHAKESHACK MENU ]
    1. Burgers         | 앵거스 비프 통살을 다져만든 버거
    2. Frozen Custard  | 매장에서 신선하게 만드는 아이스크림
    3. Drinks          | 매장에서 직접 만드는 음료
    4. Beer            | 뉴욕 브루클린 브루어리에서 양조한 맥주
    0. 종료            | 프로그램 종료
    1 <-
    
    [ Burgers MENU ]
    1. ShackBurger   | W 6.9 | 토마토, 양상추, 쉑소스가 토핑된 치즈버거
    2. SmokeShack    | W 8.9 | 베이컨, 체리 페퍼에 쉑소스가 토핑된 치즈버거
    3. Shroom Burger | W 9.4 | 몬스터 치즈와 체다 치즈로 속을 채운 베지테리안 버거
    3. Cheeseburger  | W 6.9 | 포테이토 번과 비프패티, 치즈가 토핑된 치즈버거
    4. Hamburger     | W 5.4 | 비프패티를 기반으로 야채가 들어간 기본버거
    0. 뒤로가기      | 뒤로가기
    0 <-
    
    [ SHAKESHACK MENU ]
    1. Burgers         | 앵거스 비프 통살을 다져만든 버거
    2. Forzen Custard  | 매장에서 신선하게 만드는 아이스크림
    3. Drinks          | 매장에서 직접 만드는 음료
    4. Beer            | 뉴욕 브루클린 브루어리에서 양조한 맥주
    0. 종료            | 프로그램 종료
    0 <-
    
    프로그램을 종료합니다.
    ```
    
- Lv2
    - 필요한 클래스들을 설계해요 (버거, 아이스크림, 음료, 맥주, 주문, 공통 등)
    - 클래스들의 프로퍼티와 메소드를 정의해요
    - 메소드를 이용해서 Lv1의 코드를 개선해요
        
        ![Untitled](https://teamsparta.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F03f526dc-2079-41fb-9cc9-5ccfe1623d59%2FUntitled.png?table=block&id=9629d464-d11f-4066-b167-485ef7127100&spaceId=83c75a39-3aba-4ba4-a792-7aefe4b07895&width=370&userId=&cache=v2)
        
- Lv3
    - Lv2에서 설계한 클래스들을 상속 관계를 가지도록 변경해요 (Burger도 부모 클래스를 가질 수 있을지 고민해요!)
    - 하나의 객체 리스트로 모든 메뉴들을 관리하도록 수정해요 (List)
    - ~~선택한 리스트의 요소를 삭제해요~~ (삭제된 기능입니다.)
    
    ```swift
        var 리스트변수: [클래스타입] = []
    ```
    

### 선택 구현 사항

- Lv4
    - 숫자를 입력해야하는데 문자를 입력했을때 다시 입력할 수 있도록 예외를 처리해요
    - 현재 잔액과 가격을 비교해서 구매 가능한 상태를 정의해요 (해당 기능을 담당하는 클래스를 새로 정의하셔도 됩니다.)
    
    ```bash
    "SHAKESHACK BURGER 에 오신걸 환영합니다."
    아래 메뉴판을 보시고 메뉴를 골라 입력해주세요.
    
    [ SHAKESHACK MENU ]
    1. Burgers         | 앵거스 비프 통살을 다져만든 버거
    2. Frozen Custard  | 매장에서 신선하게 만드는 아이스크림
    3. Drinks          | 매장에서 직접 만드는 음료
    4. Beer            | 뉴욕 브루클린 브루어리에서 양조한 맥주
    5 <-
    잘못된 번호를 입력했어요 다시 입력해주세요.
    6 <-
    잘못된 번호를 입력했어요 다시 입력해주세요.
    1 <-
    
    [ Burgers MENU ]
    1. ShackBurger   | W 6.9 | 토마토, 양상추, 쉑소스가 토핑된 치즈버거
    2. SmokeShack    | W 8.9 | 베이컨, 체리 페퍼에 쉑소스가 토핑된 치즈버거
    3. Shroom Burger | W 9.4 | 몬스터 치즈와 체다 치즈로 속을 채운 베지테리안 버거
    3. Cheeseburger  | W 6.9 | 포테이토 번과 비프패티, 치즈가 토핑된 치즈버거
    4. Hamburger     | W 5.4 | 비프패티를 기반으로 야채가 들어간 기본버거
    0. 뒤로가기      | 뒤로가기
    1 <-
    
    "Hamburger     | W 5.4 | 비프패티를 기반으로 야채가 들어간 기본버거"
    위 메뉴를 장바구니에 추가하시겠습니까?
    1. 확인        2. 취소
    1 <-
    
    Hamburger 가 장바구니에 추가되었습니다.
    
    "SHAKESHACK BURGER 에 오신걸 환영합니다."
    아래 메뉴판을 보시고 메뉴를 골라 입력해주세요.
    
    [ SHAKESHACK MENU ]
    1. Burgers         | 앵거스 비프 통살을 다져만든 버거
    2. Forzen Custard  | 매장에서 신선하게 만드는 아이스크림
    3. Drinks          | 매장에서 직접 만드는 음료
    4. Beer            | 뉴욕 브루클린 브루어리에서 양조한 맥주
    
    [ ORDER MENU ]
    5. Order       | 장바구니를 확인 후 주문합니다.
    6. Cancel      | 진행중인 주문을 취소합니다.
    5 <-
    
    아래와 같이 주문 하시겠습니까?
    
    [ Orders ]
    ShackBurger   | W 6.9 | 토마토, 양상추, 쉑소스가 토핑된 치즈버거
    
    [ Total ]
    W 6.9
    
    1. 주문      2. 메뉴판
    1 <-
    
    현재 잔액은 5.5W 으로 1.4W이 부족해서 주문할 수 없습니다.
    ```
    
- Lv5
    - 특정 작업이 종료된 후, 3초뒤에 다른 작업을 수행할 수 있도록 코드를 작성해요
    - 결제시 현재 시간을 비교하여 특정 시간대에는 결제할 수 없다는 알림창을 띄워줘요
    - 프로그램을 종료할때까지 5초마다 현재 주문 대기수를 실시간으로 출력해줘요 (GCD 를 이용해서 멀티쓰레드 환경을 구축해보세요.)
    
    ```bash
    아래와 같이 주문 하시겠습니까? (현재 주문 대기수: 2)
    
    [ Orders ]
    ShackBurger   | W 6.9 | 토마토, 양상추, 쉑소스가 토핑된 치즈버거
    
    [ Total ]
    W 6.9
    
    1. 주문      2. 메뉴판
    1 <-
    
    현재 시각은 오후11시 10분입니다. 
    은행 점검 시간은 오후11시 10분 ~ 오후 11시 20분이므로 결제할 수 없습니다.
    
    아래와 같이 주문 하시겠습니까? (현재 주문 대기수: 3)
    
    [ Orders ]
    ShackBurger   | W 6.9 | 토마토, 양상추, 쉑소스가 토핑된 치즈버거
    
    [ Total ]
    W 6.9
    
    1. 주문      2. 메뉴판
    1 <-
    결제를 완료했습니다. (2023-01-01 23:25:12)
    
    ```
    

예시) 

## 과제 개요


📱 내가 좋아하는 카페 또는 페스트푸드점의 키오스크를 만들어보자!

- 지금까지 배워온 Swift 언어를 사용하여 키오스크 프로그램을 만들어볼거에요.
- 내가 좋아하는 카페나 페스트푸드점의 메뉴판 데이터를 사용하면 더 재밌겠죠?


![Untitled](https://teamsparta.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F8ca4da3d-2338-41ec-ba10-84feae77273b%2FUntitled.png?table=block&id=8f5d7f2a-dfa9-4a5a-8bb4-26e08fedaeb7&spaceId=83c75a39-3aba-4ba4-a792-7aefe4b07895&width=860&userId=&cache=v2)

1. 메뉴판을 보고 주문할 수 있는 Swift 프로그램
2. 화면은 콘솔창에 심플하게 출력
3. 메뉴 클래스와 주문 클래스를 사용하여 Swift의 상속을 최대한 사용
4. 아래 View는 이해를 돕기위한 예시입니다.(뷰 적용 X)

![내가 좋아하는 메뉴를 구성해봐요!](https://teamsparta.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fc20ce0a9-0938-49b1-ab9f-d5262a50dc89%2FUntitled.png?table=block&id=aa8b9f38-d16b-41ea-ac94-f985bf26e986&spaceId=83c75a39-3aba-4ba4-a792-7aefe4b07895&width=1060&userId=&cache=v2)

내가 좋아하는 메뉴를 구성해봐요!
