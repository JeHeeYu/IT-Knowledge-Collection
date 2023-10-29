직접 공부하고 정리하는 IT 지식 모음

# Language

<details>
  <summary><h3>객체 지향 프로그래밍(OOP, Object-Oriented Programming)</h3></summary>
  객체 지향 이란 프로그래밍에서 필요한 데이터를 추상화 시켜 <b>상태와 행위를 가진 객체</b>로 만들고, 객체들 간의 상호작용을 통해 로직을 구성하는 프로그래밍 방법을 말한다.
  <br>
  객체 지향 프로그래밍은 크게 추상화, 캡슐화, 상속, 다형성 4가지의 특징을 가진다.
  <br>

  ### 추상화(Abstraction)
  추상화의 사용 이유는 다른 곳의 코드를 수정할 필요 없이, 추가로 만들 부분만 새로 생성해주면 되는 것이 가장 큰 특징이다.

  #### 추상화의 특징
  - 객체에서 공통된 속성과 행위를 추출하는 것
  - 공통의 속성과 행위를 찾아서 타입을 정의하는 과정
  - 불필요한 정보는 숨기고 중요한 정보만을 표현함으로써 프로그램을 간단하게 만드는 것

  --- 

  ### 캡슐화(Encapsulation)
  캡슐화는 속성과 기능을 정의하는 변수와 메소드를 클래스라는 캡슐에 넣어서 분류하는 것을 말한다.
  <br>
  재활용이 원활하다는 장점이 있으며 캡슐화를 통해 정보은닉(접근 제어자)을 활용할 수 있다.

  #### 캡슐화의 특징
  - 데이터 구조와 데이터 다루는 방법을 결합 시켜 묶는 것(변수와 함수를 하나로 묶는 것을 뜻함)
  - 낮은 결합도를 유지할 수 있도록 설계하는 것

  ---

  ### 상속
  상속은 클래스의 속성과 행위를 하위 클래스에 물려주거나 하위 클래스가 속성과 행위를 물려 받는 것을 말한다.
  
  #### 상속의 특징
  - 코드의 재사용을 증대 시킬 수 있음(같은 기능 재구현 필요 없음)
  - 새로운 클래스가 기존의 클래스의 데이터와 연산을 이용할 수 있음

  #### 상속의 장단점

  |장점|단점|
  |:---|:---|
  |- 재사용으로 인한 코드가 줄어듦<br>- 범용적인 사용 가능<br>- 자료와 메서드의 자유로운 사용 및 추가 가능|- 상위 클래스의 변경이 어려움<br>- 불필요한 클래스가 증가할 수 있음<br>- 상속이 잘못 상용될 수 있음|

  ---

  ### 다형성
  객체 지향 프로그래밍은 하나의 클래스 내부의 같은 이름의 메서드를 여러 개 정의하거나 상위 클래스의 행위를 하위 클래스에서 재정의하여 사용할 수 있기 때문에 다형성이라는 특징을 갖게 된다.
  <br>
  가장 큰 특징으로 오버라이딩과 오버로딩이 있다.

  #### 다향성의 특징
  - 하나의 함수명이 상황에 따라 다른 의미로 해석될 수 있는 것
  - 어떠한 요소에 여러 개의 개념을 넣어 놓은 것
    
</details>

<details>
  <summary><h3>SOLID(객체 지향 설계 원칙)</h3></summary>
  객체 지향적으로 설계하기 위해 5 가지의 원칙이 있으며, 원칙의 앞글자를 따 SOLID 원칙이라고 부른다.

  ### 1. 단일 책임 원칙(SRP, Single Responsibility Principle)
  - 하나의 클래스는 단 하나의 책임만 가져야 함
  - 단일 책임 원칙이 지켜지지 않을 경우 한 책임의 변경에 의해 다른 책임과 관련된 코드에 영향이 갈 수 있음

  ---

  ### 2. 개방-폐쇄 원칙(OCP, Open-Closed Principle)
  - 소프트웨어 요소는 확장에는 열려있으나 변경에는 닫혀 있어야 함
  - 기능을 변경하거나 확장할 수 있으면서 기능을 사용하는 코드는 수정하지 않아야 함

  ---

  ### 3. 리스코프 치환 원칙(LSP, Liskov Substitution Principle)
  - 프로그램 객체는 프로그램의 정확성을 깨뜨리지 않으면서 하위 타입의 인스턴스로 바꿀 수 있어야 함
  - 상위 타입의 객체를 하위 타입의 객체로 치환해도 상위 타입을 사용하는 프로그램은 정상적으로 동작해야 함

  ---

  ### 4. 인터페이스 분리 원칙(ISP, Interface Segregation Principle)
  - 범용 인터페이스 하나보다 클라이언트를 위한 여러 개의 인터페이스로 구성하는 것이 좋음
  - 인터페이스는 인터페이스를 사용하는 클라이언트를 기준으로 분리해야 함
  - 클라이언트가 필요로 하는 인터페이스로 분리함으로써 각 클라이언트가 사용하지 않는 인터페이스에 변경이 있어도 영향을 받지 않도록 만들어야 함

  ---

  ### 5. 의존관계 역전 원칙(DIP, Dependency Inversion Principle)
  - 추상화에 의존해야 하며, 구체화에 의존하면 안됨
  - 고수준 모듈은 저수준 모듈의 구현에 의존해서는 안됨
  - 저수준 모듈은 고수준 모듈에서 정의한 추상화 타입에 의존해야 함
    
</details>

<details>
  <summary><h3>메모리 구조</h3></summary>

  프로그램이 실행되면 프로세스 주소 공간이 메모리에 할당된다.
  <br>
  프로세스 주소 공간에는 TEXT, DATA, BSS, HEAP, STACK 영역으로 이루어져 있다.
  
  <p align="center">
    <img src="https://github.com/JeHeeYu/IT-Knowledge-Collection/assets/87363461/43c721f6-937e-48bc-b60c-c0330d5a7beb" width="230" height="460">
  </p>

  ### TEXT 영역
  Code 영역이라고도 하며, <b>실행할 프로그램의 소스 코드</b>가 들어가는 부분이다.
  <br>
  컴파일 타임에 결정되고 중간에 코드를 변경할 수 없도록 Read-Only로 지정되어 있다.

  ---

  ### DATA 영역
  프로그램의 <b>초기값이 있는</b> 전역 변수, 배열, 정적 변수가 저장되는 영역이다.
  <br>
  즉, 프로그램이 구동되는 동안 항상 접근 가능한 변수가 저장되는 영역이다.
  <br>
  <br>
  프로그램의 시작과 함께 할당되며 프로그램이 종료되면 소멸한다.
  <br>
  실행 도중 변경될 수 있으므로 Read-Write로 지정되어 있다.

  ---

  ### BSS(Block Stated Symbol) 영역
  프로그램의 <b>초기값이 없는</b> 전역 변수, 배열, 정적 변수 등이 저장되는 영역이다.
  <br>
  즉, 초기화된 데이터는 DATA 영역에, 초기화 되지 않은 데이터는 BSS 영역에 저장된다.
  <br>
  <br>
  초기화 되지 않은 변수는 프로그램이 실행할 때 영역만 잡아주면 되지만, 초기화 된 변수는 그 값도 저장하고 있어야 하기 때문이다.

  ---

  ### STACK 영역
  함수의 호출과 관계 있는 블록, 그리고 지역 변수, 매개 변수가 저장되는 영역이다.
  <br>
  함수의 호출과 함께 할당되며, 함수 호출 완료 시 소멸한다.
  <br>
  메모리의 높은 주소에서 낮은 주소 방향으로 할당된다.
  <br>
  <br>
  컴파일 타임에 크기가 결정되기 때문에 무한히 할당할 수 없다.
  <br>
  따라서 재귀 함수가 너무 깊게 호출되거나 함수가 지역 변수를 너무 많이 보유하고 있어 STACK 영역을 초기화 하면 STACK Overflow가 발생한다.

  ---

  ### HEAP 영역
  런타임 중 크기가 결정되는 메모리 영역이다.
  <br>
  사용자에 의해 메모리 공간이 동적으로 할당되고 해제된다.
  <br>
  메모리의 낮은 주소에서 높은 주소의 방향으로 할당된다.
  <br>
  <br>
  HEAP과 STACK 영역은 사실 같은 공간을 할당한다.
  <br>
  HEAP과 STACK은 서로 반대 방향으로 할당되는데, 각 영역이 상대 공간을 침범할 경우 overflow가 발생할 수 있다.

  ---
</details>

<details>
  <summary><h3>가상 함수(Virtual Function)</h3></summary>
  가상 함수란 <b>부모 클래스에서 상속 받을 클래스에서 재정의할 것으로 기대하고 정의해놓은 함수</b>를 말한다.
  <br>
  이러한 가상 함수는 자신을 호출하는 객체의 동적 타입에 따라 실제 호출할 함수가 결정된다.
  <br>
  <br>
  가상 함수는 virtual 키워드를 사용하여 선언한다.
  
  ```
  virtual 함수원형();
  ```

  <br>

  ### 바인딩(Binding)
  C++ 컴파일러는 함수를 호출할 때, 어느 블록에 있는 함수를 호출해야 하고, 해당 함수가 정확한 메모리 위치까지 알아야 한다.
  <br>
  이처럼 함수를 호출하는 코드에서 <b>어느 블록에 있는 함수를 실행하라는 의미</b>로 해석하는 것을 바인딩이라고 한다.
  <br>
  <br>
  대부분 함수를 호출하는 코드는 <b>컴파일 타임에 고정된 메모리 주소로 변환</b>된다.
  <br>
  이것을 정적 바인딩(Static Binding)이라고 한다.
  <br>
  C++에서 가상 함수가 아닌 멤버 함수는 모두 정적 바인딩을 하게 된다.
  <br>
  <br>
  하지만 가상 함수의 호출은 <b>컴파일러가 어떤 함수를 호출해야 하는지 미리 알 수 없다</b>.
  <br>
  왜냐하면, <b>가상 함수는 프로그램이 실행될 때 객체를 결정</b>하므로 컴파일 타임에 해당 객체를 특정할 수 없기 때문이다.
  <br>
  따라서 가상 함수의 경우 런 타임에 올바른 함수가 실행될 수 있도록 해야 한다.
  <br>
  이것을 동적 바인딩(Dynamic Binding) 이라고 한다.

  <br>

  ### 가상 함수 테이블(VTBL, Virtual Function Table)
  C++에서는 가상 함수의 정의와 동작 방식만을 규정하고 있으며, 그에 따른 구현은 컴파일러마다 다르다.
  <br>
  하지만 컴파일러가 가상 함수를 다루는 가장 일반적인 방식은 가상 함수 테이블을 이용하는 것이다.
  <br>
  <br>
  C++ 컴파일러는 각각의 객체마다 가상 함수 테이블을 가리키는 포인터를 저장하기 위한 숨겨진 멤버를 하나 추가한다.
  <br>
  이와 함께 가상 함수를 단 하나라도 가지는 클래스에 대해서 가상 함수 테이블을 작성한다.
  <br>
  이렇게 작성된 가상 함수 테이블에는 해당 클래스의 객체들을 위해 선언된 가상 함수들의 주소가 저장되게 된다.
  <br>
  <br>
  가상 함수를 호출하면, C++ 프로그램은 가상 함수 테이블에 접근하여 자신이 필요한 함수의 주소를 찾아 호출하게 된다.
  <br>
  가상 함수를 사용하면 이처럼 함수의 호출 과정이 복잡해지므로, 메모리와 실행 속도 측면에서 부담을 가지게 된다.
  <br>
  따라서 C++에서 <b>기본 바인딩은 정적 바인딩이며, 필요한 경우에만 가상 함수로 선언하도록</b> 하고 있다.
  > 파생 클래스가 재정의할 가능성이 있는 함수는 모두 가상 함수로 선언하는 편이 좋음

  <br>

  ### 순수 가상 함수(Pure Virtual Function)
  C++에서 가상 함수란 파생 클래스에서 재정의할 것으로 기대하는 멤버 함수를 의미한다.
  <br>
  따라서 가상 함수는 반드시 재정의해야만 하는 함수가 아닌, 재정의가 가능한 함수를 가리킨다.
  <br>
  <br>
  이와 달리 순수 가상 함수는 파생 함수는 파생 클래스에서 반드시 재정의해야 하는 멤버 함수를 의미한다.
  <br>
  이러한 가상 함수는 일반적으로 함수의 동작을 정의하는 본체를 가지고 있지 않다.
  <br>
  따라서 파생 클래스에서 재저으이하지 않으면 사용할 수 없다.
  <br>
  <br>
  아래와 같이 함수만 있고 본체가 없다는 의미로 함수 선언부 끝에 "=0"을 추가한다.

  ```
  virtual 함수 원형=0;
  ```
  
</details>

<details>
  <summary><h3>얕은 복사와 깊은 복사</h3></summary>
  
  ### 얕은 복사(Shallow Copy)
  얕은 복사는 객체가 가진 멤버들의 값을 새로운 객체로 복사하는데 만약 객체가 참조 타입의 멤버를 가지고 있다면 참조 값만 복사가 된다.
  <br>
  즉, 얕은 복사의 경우 동적 할당을 받은 변수의 주소 값을 공유한다.
  <br>
  아래는 얕은 복사의 예제 코드이다.

  ```
  #include <iostream>
  #include <cstring>
  
  using namespace std;
  
  class A
  {
  private:
      char* name;
      int age;
      
  public:
      A(char* myName, int myAge) : age(myAge)
      {
          name = new char[strlen(myName) + 1];
          strcpy(name, myName);
      }
      
      ~A()
      {
          delete []name;
          cout << "소멸자 호출" << endl;
      }
      
      void show() const
      {
          cout << "이름 : " << name << endl;
          cout << "나이 : " << age << endl;
      }
  };
  
  int main()
  {
      A a("홍길동", 20);
      A b = a;
      
      a.show();
      b.show();
  
      return 0;
  }

  // 실행 결과
  이름 : 홍길동
  나이 : 20
  이름 : 홍길동
  나이 : 20
  소멸자 호출
  ```

  A클래스의 객체 a와 b가 있으며, a는 객체 생성 시 초기화를 했다.
  <br>
  반면 b는 a의 디폴트 복사 생성자에 의해 멤버 대 멤버 복사가 일어났다.
  <br>
  즉, 여기서 얕은 복사가 일어났다.
  <br>
  <br>
  근데 객체는 2개이나, 소멸자가 한 번만 호출 되었다.
  <br>
  그 이유는 char* 포인터인 name 때문이다.
  <br>
  멤버 대 멤버 복사이기 때문에 객체 a의 name을 가리키는 주소 값을 b도 같이 할당 받아 두 객체가 같은 문자열을 참조하는 문제가 생긴다.
  <br>
  <br>
  그래서 만약 객체 a가 소멸된다고 가정하면 a의 소멸자 호출이 일어나면서 delete를 해준다.
  <br>
  하지만 b의 소멸자 호출이 일어나면 이미 소멸된 문자열을 대상으로 delete 하기 때문에 문제가 발생한다.
  <br>
  하지만 변수가 힙의 메모리 공간을 참조하지 않는다면 별다른 문제가 생기지 않는다.
  <br>
  <br>
  이처럼 얕은 복사는 간단하지만 멤버 변수에 따른 문제점이 발생하는 것을 고려해야 한다.

  <br>

  ### 깊은 복사(Deep Copy)
  깊은 복사는 전체 복사로 생각할 수 있다.
  <br>
  얕은 복사와 달리 객체가 가진 모든 멤버를 복사하는 것을 말한다.
  <br>
  객체가 참조 타입의 멤버를 포함할 경우 참조 값의 복사가 아닌 참조된 객체 자체가 복사되는 것을 말한다.
  <br>
  <br>
  즉, 깊은 복사는 새로 동적 할당을 받고, 원본의 데이터를 복사한다.
  <br>
  아래는 깊은 복사의 예제 코드이다.

  ```
  #include <iostream>
  #include <cstring>
  
  using namespace std;
  
  class A
  {
  private:
      char* name;
      int age;
      
  public:
      A(char* myName, int myAge) : age(myAge)
      {
          name = new char[strlen(myName) + 1];
          strcpy(name, myName);
      }
      
      A(const A &copy) : age(copy.age)
      {
          name = new char[strlen(copy.name) + 1];
          strcpy(name, copy.name);
      }
      
      ~A()
      {
          delete []name;
          cout << "소멸자 호출" << endl;
      }
      
      void show() const
      {
          cout << "이름 : " << name << endl;
          cout << "나이 : " << age << endl;
      }
  };
  
  int main()
  {
      A a("홍길동", 20);
      A b = a;
      
      a.show();
      b.show();
  
      return 0;
  }

  // 실행 결과
  이름 : 홍길동
  나이 : 20
  이름 : 홍길동
  나이 : 20
  소멸자 호출
  소멸자 호출
  ```
  

  기존의 얕은 복사에서는 소멸자가 한 번만 호출되었다면 여기서는 두 번 호출되었다.
  <br>
  복사 생성자에서 const를 인자로 받는데, 그 이유는 기존의 객체의 멤버 변수 값을 건드리지 않겠다는 의미이다.

  <br>

  ### 복사 생성자(Copy Constructor)
  C++에서 복사 생성자란 자신과 <b>같은 클래스 타입의 다른 객체에 대한 참조를 인수로 전달 받아 그 참조를 가지고 자신을 초기화</b>하는 방법이다.
  <br>
  복사 생성자는 새롭게 생성되는 객체가 원본 객체와 같으면서도, 완전한 독립성을 가지게 해준다.
  <br>
  왜냐하면 복사 생성자를 이용한 대입은 깊은 복사를 통한 값이기 때문이다.
  <br>
  <br>
  복사 생성자는 다음과 같은 상황에서 주로 사용된다.
  - 객체가 함수에 인수로 전달될 때
  - 함수가 객체를 반환 값으로 반환할 때
  - 새로운 객체를 같은 클래스 타입의 기존 객체와 똑같이 초기화할 때
</details>

<br>

# Operating System

<details>
  <summary><h3>프로세스 스케줄링 종류와 기법</h3></summary>

  ## 스케줄링
  스케줄링이란 프로세스가 생성되어 실행될 때 필요한 시스템의 여러 자원을 해당 프로세스에게 할당하는 작업을 말한다.
  <br>
  대기 시간은 최소화하고 최대한 공평하게 처리하는 것을 목적으로 둔다.

  <br>

  ### 스케줄링의 종류
  스케줄링의 종류로 크게 2가지가 있다.
  - 선점(Preemptive) 스케줄링
  - 비선점(Non-Preemptive) 스케줄링

  <br>

  ## 선점 스케줄링
  - 하나의 프로세스가 CPU를 차지하고 있을 때, 우선순위가 높은 다른 프로세스가 현재 프로세스를 중단시키고 CPU를 점유하는 스케줄링 방식
  - 비교적 응답이 빠른 장점이 있음
  - 처리 시간을 예측하기 힘들고 높은 우선순위 프로세스들이 계속 들어오는 경우 오버헤드가 발생할 수 있음

  <br>

  ### 라운드 로빈(Round Robin)
  - 프로세스마다 같은 크기의 CPU 시간을 할당(시간 할당량 / Time Slice / Quantum) - 보통 10 ~ 100ms 정도의 시간
  - 프로세스가 할당된 시간 내에 처리되지 않으면 준비 큐 리스트의 가장 뒤로 보내지고, CPU는 대기 중인 다음 프로세스로 넘어감
  - 균등한 CPU 점유 시간을 보장하며, 시분할 시스템에 사용

  <br>

  ### SRT(Shortest Remaning Time First)
  - 가장 짧은 시간이 소요되는 프로세스를 먼저 수행
  - 남은 시간이 더 짧다고 판단되는 프로세스가 준비 큐에 생기면 언제라도 프로세스가 점령됨

  <br>

  ### 다단계 큐(Multi Level Queue)
  - 작업들을 여러 종류 그룹으로 분할하고 여러 개의 큐를 이용하여 상위 단계 작업이 선점
  - 각 큐는 자신만의 독자적인 스케줄을 가짐

  <br>

  ### 다단계 피드백 큐(Multi Level Feedback Queue)
  - 입출력 위주와 CPU 위주인 프로레스의 특성에 따라 큐마다 서로 다른 CPU 시간 할당량 부여
  - FCFS와 라운드 로빈 기법 혼합
  - 새로운 프로세스는 높은 우선순위를 가지지만, 프로세스의 실행 시간이 길어질 수록 점점 낮은 우선순위 큐로 이동하며, 마지막 단계에서 FCFS 방식 적용
  - 유연성이 뛰어나며, Turnadround 시간과 Response Time에 최적화

  <br>

  ## 비선점 스케줄링
  - 이미 할당된 CPU를 다른 프로세스가 강제로 빼앗아 사용할 수 없는 스케줄링 기법
  - 프로세스가 CPU를 할당 받으면 해당 프로세스가 완료될 때까지 CPU를 사용하지 않음

  <br>

  ### 우선순위(Priority)
  - 각 프로세스 별로 우선순위가 주어지고, 우선순위에 따라 CPU 할당
  - 우선순위가 같을 경우 FCFS 적용
  - 설정, 자원 상황 등에 따른 우선순위를 선정해 주요(긴급) 프로세스에 대한 우선순위 처리 가능

  <br>

  ### 기한부(Deadline)
  - 작업들이 명시된 기간이나 기한 내에 완료되도록 계획

  <br>

  ### FCFS(First Come First Serve Scheduling) 스케줄링
  - CPU를 먼저 요청한 프로세스가 먼저 CPU를 배정 받는 스케줄링 기법
  - 프로세스가 대기 큐에 도착한 순서에 따라 CPU 할당

  <br>

  ### SJF(Shortest Job First)
  - 프로세스가 도착하는 시점에 따라 그 당시 작은 서비스 기간을 갖는 프로세스가 종료 시 까지 선점
  - 준비 큐 작업 중 가장 짧은 작업부터 수행하므로 평균 대기시간 최소화
  - CPU 요구 시간이 긴 작업과 짧은 작업 간의 불평등이 심하여, CPU 요구 시간이 긴 프로세스는 기아 현상 발생

  <br>

  ### HRN(Highest Response Ratio Next)
  - 대기 중인 프로세스 중 현재 응답 비율(Response Ratio)이 가장 높은 것을 선택
  - (Response Ratio = (대기 시간 + 서비스 시간) / 서비스 시간)
  - 대기 시간이 긴 프로세스일 경우 우선순위가 높아짐
  - 긴 작업과 짧은 작업 간의 지나친 불평등 해소 가능
  
</details>


<br>

# Algorithm

<details>
  <summary><h3>Tree</h3></summary>

  ## Tree란?
  Tree는 **계층구조**를 가진 데이터 구조로, 부모-자식 개념을 가지는 **비선형 개념**의 Graph 자료구조의 일종이다.
  <br>
  트리 구조를 그림으로 나타낼 때는 실제 나무와는 반대로 뿌리가 맨 위에 나타내는 상하 반전된 형태로 표현한다.
  <br>
  <br>
  트리는 하나의 루트 노드(Root Node)를 가지며, 이 노드는 트리의 가장 맨 위에 존재한다.
  <br>
  루트 노드는 1개 이상의 자식 노드를 가지게 된다.
  <br>
  <img src="https://github.com/JeHeeYu/IT-Knowledge-Collection/assets/87363461/2f6016d3-2aad-4226-811e-382a99498ff5" width="700" height="300">
  <br>
  <br>
  ## Tree 특징
  - 계층 구조를 가지는 **계층 모델**
  - DAG(Directed Acyclic Graphs, 방향성이 없는 비순환 그래프) 의 한 종류로, Loop, Circuit이 없음, 즉 **사이클이 없음**
  - 노드가 N개인 트리는 **항상 N-1 개의 간선을 가짐**
  - 루트에서 어떤 노드로 가는 경로는 유일함
  - 임의의 노드 간 경로는 유일함, 즉 두 개의 정점 사이에 반드시 1개의 경로만을 가짐
  <br>
  
  
  ## Tree 용어
  - **루트 노드(Root Node)** : 부모가 없는 노드로 트리는 하나의 루트 노드만을 보유함
  - **단말 노드(Leaf Node)** : 자식이 없는 노드로 ‘말단 노드’ 또는 ‘잎 노드’라고도 함
  - **내부 노드(Internal Node)** : 단말 노드가 아닌 노드
  - **간선(Edge)** : 노드를 연결하는 선(Link, Branch 라고도 함)
  - **형제(Sibling)** : 같은 부모를 가지는 노드(형제 노드라고도 함)
  - **노드의 크기(Size)** : 자신을 포함한 모든 자식 노드의 개수
  - **노드의 깊이(Depth)** : 루트에서 어떤 노드에 도달하기 위해 거쳐야 하는 간선의 수
  - **노드의 레벨(Level)** : 트리의 특정 깊이를 가지는 노드의 집합
  - **노드의 차수(Degree)** : 하위 트리 개수 / 간선 수 (Degree) = 각 노드가 지닌 가지의 수
  - **트리의 차수(Degree of Tree)** : 트리의 최대 차수
  - **트리의 높이(Height)** : 루트 노드에서 가장 깊숙히(맨 아래) 있는 노드의 깊이

  <br>

  ## 트리 순회(Traversal) 방법
  트리의 순회 방법으로 전위(Prorder) 순회, 중위(Inorder) 순회, 후위(Postorder) 순회가 있다.

  ### 전위 순회(Preorder)
  전위 순회는 노드를 먼저 방문하고 그 다음 현재 노드의 왼쪽 하위 노드를, 마지막으로 하위 노드를 재귀적으로 방문하는 방법을 말한다.
  ```
  void preOrderTraversal(TreeNode node) {
      if(node != null) {
          visit(node);
          preOrderTraversal(node.left);
          preOrderTraversal(node.right);
    }
  }

  ```
  <p align="center">
    <img src="https://github.com/JeHeeYu/IT-Knowledge-Collection/assets/87363461/e5f6a5b8-fb70-4704-a0f1-9e651e5999c0" width="400" height="200">
  </p>
  <br>

  ### 중위 순회(Inorder)
  중위 순회는 왼쪽 노드를 먼저 방문하고, 그 다음 현재 노드, 마지막으로 오른쪽 노드를 방문하는 방법을 말한다.
  ```
  void inOrderTraversal(TreeNode node) {
      if(node != null) {
          inOrderTraversal(node.left);
          visit(node);
          inOrderTraversal(node.right);
      }
  }
  ```
  <p align="center">
    <img src="https://github.com/JeHeeYu/IT-Knowledge-Collection/assets/87363461/52e88a8d-0c20-456f-811c-ecea1e28c442" width="400" height="200">
  </p>
  <br>

  ### 후위 순회(Postorder)
  후위 순회는 두 자식 노드를 먼저 방문한 후 현재 노드를 방문하는 방법을 말한다.
  ```
  void postOrderTraversal(TreeNode node) {
      if(node != null) {
          postOrderTraversal(node.left);
          postOrderTraversal(node.right);
          visit(node);
      }
  }
  ```

  <p align="center">
    <img src="https://github.com/JeHeeYu/IT-Knowledge-Collection/assets/87363461/69a85296-da18-4671-9dc0-28c1f7ed88c3" width="400" height="200">
  </p>
  <br>
  
</details>

<br>

# Network

<details>
  <summary><h3>네트워크 형태</h3></summary>  

  ## 근거리 영역 네트워크(LAN, Local Area Network)
  근거리 영역 네트워크는 건물안의 범위나 특정 지역에서 사용하는 네트워크를 말한다.
  <br>
  유선 케이블, 적외선 링크, 무선 송수신기 등을 이용한다.
  <br>
  한 건물 또는 인접한 건물군 내에 있는 네트워크는 하나의 LAN으로 간주된다.

  <br>

  <p align="center">
    <img src="https://github.com/JeHeeYu/IT-Knowledge-Collection/assets/87363461/d4c5b907-6f70-4b75-b384-5fde9686db7b" width="800" height="400">
  </p>

  <br>

  ### LAN의 특징
  - 단일 기관의 소유 또는 제한된 지역 내의 통신
  - 광대역 전송 매체의 사용으로 고속 통신 가능
  - 공유 매체를 사용하므로 경로 선택 없이 매체에 연결된 모든 장치로 데이터 전송 가능
  - 오류 발생률이 낮으며 네트워크에 포함된 자원 공유 가능
  - 네트워크의 확장 또는 재배치 용이
  - 망의 구성 형태에 따라 성(스타)형, 버스형, 링형, 계층(트리)형으로 분류
  - 전송 매체로 꼬임선, 동축 케이블, 광섬유 케이블 등을 이용

  <br>

  ### LAN의 장단점
  **장점**
  - 통신 선로가 가장 짧아 제어가 간단하며 관리 및 확장이 용이함
  - 통신망 신뢰도가 높음
  - 상대적으로 낮은 비용이 드는 매체로 높은 대역폭 이용 가능
  - 게이트웨이, 브리지, 라우터 등의 네트워크 장비를 이용하여 다른 네트워크와 연동 가능
  - 다양한 응용을 수용할 수 있으며 많은 수의 단말 장치 연결 가능
  - 네트워크 관리 용이

  **단점**
  - 네트워크 중앙에 병목현상 가능성이 있음
  - 짧은 거리에서의 통신망을 지원하므로, 거리를 확장하기 위해 리피터, 허브, 브리지와 같은 네트워크 장비가 필요함

  <br>

## 광역 네트워크(WAN, Wide Area Network)
  광역 네트워크는 2개 이상의 LAN을 넓은 지역에 걸쳐 연결한 것을 말한다.
  <br>
  원거리에 있는 네트워크의 경우 라우터나 스위치에 묶을 수 없는 한계가 존재하기 때문에 이런 경우 네트워크 간의 연결을 위해 WAN을 사용한다.
  <br>
  <br>
  또한 LAN에 포함되지 않은 원격의 컴퓨터들도 WAN을 이용하여 서로 통신할 수 있다.
  <br>
  <br>
  WAN은 ISP(인터넷 서비스 제공자)가 제공하는 서비스를 사용하여 구축된 네트워크이다.
  <br>

  <p align="center">
    <img src="https://github.com/JeHeeYu/IT-Knowledge-Collection/assets/87363461/7a097d26-d527-47dd-b4bf-0cd624610ac5" width="800" height="400">
  </p>

  <br>

  ### WAN의 특징
  - 지역성 제한이 없음
  - 여러 LAN과 상호 작용함
  - LAN보다 복잡하고 어려움
  - 기술적 비용이 많이 발생함

  <br>

  ### WAN의 장단점
  **장점**
  - 넓은 범위이기 때문에 어디에서나 사용할 수 있는 유연성
  - 필요에 따라 새로운 위치나 지점을 추가하거나 기존 네트워크를 확장이 비교적 간단함
  - 긴 거리 통신을 지원함
    
  **단점**
  - LAN에 비해 거리가 길기 때문에 신호가 약해지거나 오류가 발생할 확률이 있음
  - 거리가 멀어지는 만큼 LAN에 비해 속도가 느림
  - 대역폭이 제한적이므로 대용량 데이터의 전송에 어려움이 있음
  - WAN을 설정하고 유지하는데 높은 비용이 발생함

  <br>

  ## 도시권 통신망(MAN, Metropolitan Area Network)
  도시권 통신망은 큰 도시 또는 캠퍼스에 퍼져 있는 네트워크이다.
  <br>
  MAN은 LAN보다 큰 규모를 가지지만 WAN보다는 작은 중간 크기 규모의 네트워크이다.
  <br>
  <br>
  대표적인 예로 DSL 전화망, 케이블 TV 네트워크를 통한 인터넷 서비스 제공이 있다.

  <br>

  <p align="center">
    <img src="https://github.com/JeHeeYu/IT-Knowledge-Collection/assets/87363461/7ad83b92-5b03-47d2-a7f3-e0ffe1045133" width="400" height="200">
  </p>

  <br>

  ### MAN의 특징
  - LAN에 비해 넓은 지리적 범위를 가지며, 일반적으로 도시 또는 국가의 한 지역을 커버함
  - MAN은 고속 데이터 전송을 지원하므로 여러 지점 간 빠른 데이터 공유 가능
  - MAN은 고성능 네트워크 요구 사항을 충족시키기 위해 설계되며 신속한 데이터 액세스를 지원함
  - 가상 LAN(VLAN)을 사용하여 여러 위치 간의 논리적인 분리를 가능하게 하여 보안 및 트래픽 관리 강화 가능

  <br>

  ### MAN의 장단점
  **장점**
  - 고속 데이터 전송을 지원하므로 근거리 지점 간 빠른 데이터 공유 가능
  - WAN에 비해 근거리 지역이므로 집중적인 서비스 제공 가능
  - 중요한 비즈니스 및 정부 기관과 같은 기관에서 사용되므로 높은 신뢰성
  - 지리적으로 제한된 네트워크이므로 관리가 상대적으로 간단함

  **단점**
  - WAN에 비해 작은 영역이므로 국가 간의 연결을 제공하지 못함
  - 고성능의 네트워크에 장비 및 라우팅 인프라를 구축할 때 높은 비용이 발생할 수 있음
  - 도시 또는 지역 내의 새로운 지점을 추가하거나 확장하는 것이 어려움
  - 특정 도시나 근거리에 적합하므로 원격 지역이나 농촌 지역에는 적합하지 않음

  <br>

  ## 인트라넷(Intranet)
  인트라넷은 기업이나 조직 내부에서 사용하는 전용 네트워크를 말한다.
  <br>
  인터넷과 유사한 기술을 사용하지만 내부 사용자만을 위한 목적으로 구축되는 특수한 형태의 네트워크이다.
  <br>
  <br>
  인트라넷을 이용하면 조직 내에서 관리되는 문서, 메신저, 게시판 등을 공개되지 않는 웹 페이지에서 처리할 수 있다.

  <br>

  <p align="center">
    <img src="https://github.com/JeHeeYu/IT-Knowledge-Collection/assets/87363461/bbb6d602-6be2-4dbf-9c74-cc2d40253bac" width="400" height="200">
  </p>

  <br>

  ### 인트라넷의 특징
  - 조직 내부에서만 사용되는 전용 네트워크
  - 민감한 정보와 데이터 보호
  - 외부 액세스가 제한되며 내부에서만 접속 가능
  - 조직의 크기 및 요구 사항에 따라 확장 용이


<br>

  ### 인트라넷의 장단점
  **장점**
  - 중요한 정보와 데이터를 보호하고 있어 보안에 강함
  - 조직 내에서 효율적인 의사 소통과 협업 촉진
  - 문서, 데이터 및 애플리케이션 공유로 업무 효율성 향상 가능
  - 종이 문서 및 물리적 자료 사용을 줄이고 디지털 프로세스로 비용 절감 가능

  **단점**
  - 외부 액세스가 제한되므로 원격 근무 협업 불가
  - 인트라넷 구축 및 유지 관리 초기 비용이 발생
  - 사용자의 권한, 보안 정책 등을 관리하기 위핸 복잡성 증가
  
  
</details>


  

<br>

# Database

- [트랜잭션(Transaciton)](https://github.com/JeHeeYu/IT-Knowledge-Collection/blob/main/Database/%ED%8A%B8%EB%9E%9C%EC%9E%AD%EC%85%98(Transaction)/README.md)

<br>

# Embedded

<details>
  <summary><h3>ARM 구성 Register</h3></summary>
  ARM 프로세서는 32비트 길이의 레지스터를 총 40개 가지고 있다.
  <br>
  <br>
  데이터 연산 시 사용하는 <b>범용 레지스터(General Purpose Register) 32개</b>,
  <br>
  프로세서의 동작 상태를 나타낼 때 사용하는 <b>상태 레지스터(Status Register) 7개</b>,
  <br>
  프로그램을 제어할 때 사용하는 <b>프로그램 카운터(PC, Program Counter) 1개</b>로 구성되어 있다.
  
  <br>

  ### 범용 레지스터(General Purpose Register)
  범용 레지스터는 <b>데이터 처리 또는 데이터 전송</b> 등 다양한 목적으로 사용된다.
  <br>
  32개의 범용 레지스터는 8가지의 ARM 동작 모드에서 공유하여 사용하는 레지스터와 각 동작 모드별로 할당된 레지스터가 있다.
  <br>
  각 동작 모드별로 할당되는 레지스터는 서로 다른 동작 모드에서는 사용할 수 없다.

  ---

  ### 프로그램 카운터 레지스터(Program Counter Register)
  프로그램 카운터란 프로그램을 읽어올 메모리 위치를 나타낸다.
  <br>
  즉, <b>다음 실행될 명령어 주소를 가지고 있는 레지스터이다.</b>
  <br>
  <br>
  ARM 상태에서는 [31:2]에 읽어올 명령어의 어드레스를 저장하면 비트[1:0]은 0으로 채워지고,
  <br>
  Thumb 상태에서는 [31:1]에 어드레스를 저장하고 비트[0]은 0으로 채워진다.
  <br>
  <br>
  1개만 존재하는 프로그램 카운터 레지스터는 모든 동작 모드에서 공유하여 사용된다.

  ---

  ### 상태 레지스터(Status Register)
  상태 레지스터는 프로세서의 동작 상태를 나타내는 레지스터로, 6개의 SPSR, 1개의 CPSR 총 7개의 레지스터로 구성된다.

  <br>

  ### SPSR(Saved Program Status Register)
  SPSR은 이전 동작 모드의 CPSR을 복사해 보관하는 레지스터이다.
  <br>
  즉, CPSR과 표현되는 정보가 동일하다.
  <br>
  <br>
  ARM 모드에서 유저 모드, 시스템 모드 2가지를 제외한 나머지 모드에서는 예외 처리에 의해 모드 전환이 이루어 지는데, 모드 전환이 이루어지는 이 때 이전 동작 모드의 CPSR을 복사해 SPSR이 보관한다.
  <br>
  <br>
  SPSR은 유저 모드, 시스템 모드를 제외하고 각각 개의 동작 모드에서 1개씩 할당되어 사용된다.

  ---

  ### CPSR(Current Program Status Register)
  CPSR은 <b>현재 동작 중인 프로세서의 상태를 나타내고 있는</b> 레지스터이다.
  <br>
  프로세서의 상태란 프로세스의 동작 모드(8가지), 수행되는 명령어의 종류(ARM, Thumb)를 나타낸다.
  <br>
  <br>
  추가로 연산 결과가 0 또는 캐리(Carry)가 발생했는지, 오버플로우(Overflow)가 발생했는지에 대한 정보도 가지고 있다.
  <br>
  이 레지스터를 이용하여 인터럽트 돚악 모드인 IRQ 또는 FIQ를 켜거나 끌 수 있다.
  <br>
  <br>
  ARM의 8가지 동작 모드에서 모듀 공유해서 사용한다.

  ---

  <br>

  ### ARM 명령어 상태의 동작 모드 레지스터
  ARM 프로세서는 각각의 동작 모드에서 사용할 수 있는 <b>범용 레지스터가 PC까지 포함 총 16개로 구성</b>되어 있다.
  <br>
  각각의 범용 레지스터는 <b>R0부터 R15까지 이름이 부여</b>되어 있으며, R15는 PC의 사용 용도에 따라 R15 또는 PC로 사용되기도 한다.
  <br>
  <br>
  PC는 일반 범용 레지스터와 동일하게 각종 데이터 처리나 데이터 전송에도 자유롭게 사용될 수 있다.
  <br>
  PC를 포함한 대부분의 레지스터는 모든 동작 모드에서 공유된다.
  <br>
  다른 일부 레지스터들은 동작 모드별로 사용한다.
  <br>
  <br>
  별도로 할당된 레지스터는 대부분 특수한 목적으로 사용되는데, 이 레지스터는 R13과 R14가 있다.

  <br>

  #### 스택 포인터(Stack Pointer) - R13 or SP
  범용 레지스터 중 R13은 R13 또는 스택포인터로 사용될 수 있는 레지스터이다.
  <br>
  스택 포인터는 프로그램에서 사용하는 메모리 중 TOP 위치를 저장한다.

  <br>

  #### 링크 레지스터(Rink Register) - R14 or LR
  범용 레지스터 중 R14는 R14 또는 링크 레지스터로 사용될 수 있는 레지스터이다.
  <br>
  링크 레지스터는 서브 루틴 함수에서 되돌아갈 주소를 저장하거나 예외 처리 후 돌아갈 주소를 저장하는 레지스터이다.

  <p align="center">
    <img src="https://github.com/JeHeeYu/IT-Knowledge-Collection/assets/87363461/c46894f3-342f-4d94-84d5-ea10fea0e9f3" width="380" height="360">
  </p>

  표에서 색이 파란색으로 표시된 레지스터 R13, R14, SPSR은 각각 모드에 따라 별도로 할당되어 사용됨을 뜻한다.
  <br>
  흰색으로 표시된 레지스터 R0 ~ R12, R15(PC), CPSR은 모든 동작 모드에서 공유하여 사용하는 것을 뜻한다.
  <br>
  <br>
  다른 동작 모드와는 다르게 RIQ 모드에서는 R8 ~ R12까지도 별도로 할당된 레지스터를 사용한다.
  <br>
  <br>
  여기서 별도로 할당된 레지스터라는 뜻은 그 레지스터 안에 들어있는 값을 읽을 때, 해당 모드에서만그 값을 확인할 수 있는 것을 말한다.
  
</details>

<details>

  <summary><h3>ARM 프로세서의 동작 모드</h3></summary> 

  ARM 프로세서의 동작 모드는 프로세스가 어떤 권한을 가지고 어떤 종류의 작업을 처리하는지 나타낸다.
  <br>
  ARM에서 제공하는 모드는 총 8가지의 모드가 있다.
  <br>
  <br>
  유저 모드와 시스템 모드는 프로그래밍을 통해 변경이 가능하고, 나머지 모드는 외부의 요청 또는 오류에 의해 이루어진다.
  <br>
  <br>
  ARM에는 상태 레지스터(Status Register)가 있는데, 이 레지스터에 값을 수정하여 각각의 동작 모드를 설정할 수 있다.

  <br>
  
  ### 유저(User) 모드
  유저 모드는 ARM이 User Task, Application 등을 수행할 때의 동작 모드이다.
  <br>
  유저 모드는 다른 모드들과 다르게 유일한 비특권(Un-Privilleged) 모드이다.
  > 특권 모드란 프로세서의 동작을 위한 모드로, 프로세서의 모든 메모리 접근 및 명령이 가능한 모드를 말함
  <br>
  즉, 일반 사용자의 모드를 나타내고, 메모리, I/O 장치 등과 같은 시스템 자원 사용에 제한을 두고, 사용자의 실수를 미연에 방지하는 목적으로 활용할 수 있다.

  ---

  ### 시스템(System) 모드
  시스템 모드는 유저 모드와 동일한 용도로 사용된다.
  유저 모드의 특별한 모드 느낌이다.
  <br>
  <br>
  유저 모드와 다른 점은 ARM 프로세서 내부의 CPSR을 완전히 읽고 쓸 수 있으며, 특권 모드이다.
  > CPSR(Current Program Status Register)는 ARM 프로세서의 세부 상태를 저장하는 용도로 사용됨

  ---

  ### IRQ(Interrupt ReQuest) 모드
  IRQ 모드는 ARM에서 사용하는 일반적인 인터럽트를 처리하는 모드이다.
  <br>
  외부 장치에서 요청되는 IRQ의 발생에 의해 ARM 프로세서는 IRQ 모드로 전환 후 인터럽트 작업을 처리한다.
  
  ---
  
  ### FIQ(Fast Interrupt reQuest) 모드
  FIQ 모드는 IRQ와 같이 인터럽트를 처리하는 모드인데, 인터럽트 중에서 빠르게(Fast) 인터럽트를 처리하는 모드를 말한다.
  <br>
  외부 장치에서 요청되는 FIQ의 발생에 의해 ARM 프로세서는 FIQ 모드로 전환 후 인터럽트 작업을 처리한다.
  <br>
  <br>
  빠른 처리를 위해 Exception Vector 에서도 최하단에 존재하고 별도의 레지스터를 보유한다.
  
  ---
  
  ### SVC(Supervisor) 모드
  SVC 모드는 시스템 자원 대부분을 자유롭게 관리할 수 있는 모드이다.
  <br>
  커널이나 디바이스 드라이버를 처리할 때 사용(System Call)하는 모드이기도 하다.
  <br>
  <br>
  외부에서 Reset 신호 또는 SWI(SoftWare Interface) 신호가 발생하면 SVC 모드로 전환된다.

  ---

  ### Abort 모드
  Abort 모드는 메모리에서 명령을 읽을 경우 또는 데이터를 읽거나 쓸 때 오류가 발생하면 전환되는 모드이다.
  <br>
  ARM 프로세서는 Abort 모드로 전환하여 메모리 오류를 처리한다.
  <br>
  <br>
  발생하는 오류는 MMU, MPU 또는 외부의 메모리 제어기에서 구동되는 Abort 신호에 의해서 발생된다.

  ---

  ### Undefined 모드
  Undefined 모드는 ARM 내부에서 명령어를 읽어 실행하고자 할 때 읽어온 명령이 디코더에 정의되어 있지 않은 명령어인 경우 발생되는 오류를 처리하기 위한 동작 모드이다.

  ---

  ### 모니터(Monitor) Mode
  모니터 모드는 ARM 프로세서 중 트러스트존(Trust Zone)을 지원하는 프로세서는 보호(Security) 영역과 비보호(Non-Security) 영역으로 공간을 구분해주는 기능을 제공하기 때문에 데이터와 프로그램을 적절하게 관리할 수 있다.
  <br>
  <br>
  모니터 모드는 보호 영역과 비보호 영역 사이의 모드 변경을 처리하기 위한 모드이다.
  <br>
  모니터 모드는 초기 ARM 버전에서는 없었던 모드로, 비교적 최근에 생긴 모드이다.
  <br>
  그래서 이전 ARM 모드는 총 7가지 였다.


</details>
