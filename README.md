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
  트리의 순회 방법으로 전위(Pre-Order) 순회, 중위(In-Order) 순회, 후위(Post-Order) 순회가 있다.

  ### 전위 순회(Pre-Order)
  전위 순회는 노드를 먼저 방문하고 그 다음 현재 노드의 왼쪽 하위 노드를, 마지막으로 하위 노드를 재귀적으로 방문한다.
</details>

# Database

- [트랜잭션(Transaciton)](https://github.com/JeHeeYu/IT-Knowledge-Collection/blob/main/Database/%ED%8A%B8%EB%9E%9C%EC%9E%AD%EC%85%98(Transaction)/README.md)
