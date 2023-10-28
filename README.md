직접 공부하고 정리하는 IT 지식 모음

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

  <summary><h3>ARM 레지스터 종류</h3></summary> 

  ARM 프로세서의 동작 모드는 프로세스가 어떤 권한을 가지고 어떤 종류의 작업을 처리하는지 나타낸다.
  <br>
  ARM에서 제공하는 모드는 총 8가지의 모드가 있다.
  <br>
  <br>

  ### User 모드

  
  
</details>
