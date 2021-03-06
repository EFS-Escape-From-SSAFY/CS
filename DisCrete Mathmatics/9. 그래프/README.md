### 그래프

#### 현실 문제를 모델링하여 문제를 해결하기 위하여 사용

#### 그래프의 정의

- 그래프 G는 다음의 두 가지 집합으로 구성되며 G={V,E}로 표시한다.
- 여기서 V는 정점(Vertex)들의 집합이며
- E는 정점들을 연결하는 선(edge)의 집합이다.

#### 기본용어

- 인접 : e=(u,v)에 대해서 정점 u와 v는 서로 인접
- 접합 : e=(u,v)에 대해서 e는 정점 u와 v에 접합
- 루프 : 연결선의 두 끝점이 같은 정점인 연결선
- 다중연결선 : 두 정점의 연결선이 두 개 이상
- 단순그래프 : 루프나 다중 연결선이 없는 그래프
- 차수 : 정점 u에 접합된 연결선의 수(deg(u))
  - 그래프에서 모든 정점의 차수의 합은 모든 연결선 수의 2배이다.
- 길이 : 두 정점의 경로를 구성하는 연결선의 수
- 거리 : 두 정점 간의 최단 경로의 길이
- 닫힌 경로 : 시작점과 끝점이 같은 경로
- 순환 : 3개 이상의 연결선을 갖는 경로에서 어떤 연결선도 중복되지 않는 닫힌 경로
- 부분 그래프 : 그래프 G의 부분집합
- 동형 그래프 : 다르게 보이게 그릴 수 있지만 모양이 같은 그래프
- 완전 그래프 : 그래프가 모든 정점 사이에 연결선이 존재한다.
- 이분 그래프 : 정점들이 두 집합으로 나누어지고 다른 집합의 정점에만 연결선을 갖는 그래프
- 완전 그래프 : 이분 그래프중 다른 집합의 모든 정점에 연결선을 갖는 그래프
- 정규 그래프 : 모든 정점의 차수가 같은 그래프
- 평면 그래프 : 연결선들이 서로 <b>교차하지 않고</b> 평면상에 그릴 수 있는 그래프
- 면 : 연결선에 따라 구분된 영역
- 방향 그래프 : 연결선에 방향이 있는 그래프
- 

### 오일러

#### 오일러 경로

- 그래프 G의 모든 <b>연결선</b>을 한번만 방문하는 경로

#### 오일러 순환

- 시작점과 끝점이 동일한 오일러 경로

#### 오일러 그래프

- 오일러 순환이 존재하는 그래프

#### 차수

- 정점 u에 접합된 연결선의 수
- 차수는 deg(u)와 같이 표기하기도 한다.

#### 

#### 오일러 순환을 찾는 알고리즘

- 2개 이상의 정점을 갖는 루프가 없는 연결 그래프에서 홀수 차수를 갖는 정점이 하나도 없거나 오직 두개(시작점,도착점)만 존재해야한다.
- 특히, 모든 정점이 짝수 차수를 가지면 오일러 순환이 존재하며, 이 그래프는 오일러 그래프이다.
- 시간복잡도 O(n2)

### 

### 해밀턴

#### 해밀턴 경로

- 그래프 G에서 모든 <b>정점</b>을 정확히 한번만 지나는 경로

#### 해밀턴 순환

- 시작점과 끝점이 같은 해밀턴 경로

#### 해밀턴 순환을 찾는 알고리즘

- 모든 경우를 탐색해야한다.(전수 조사)
- 시간복잡도 O(xn)
- 유사한 복잡도 문제(np)
  - 암호 해독, 바둑, 장기, chess 등

#### 방문 판매원 문제(TSP)

- 연결선에 비용이 주어진다.
- 일반적으로 완전 그래프
- 비용이 최소가 되는 해밀턴 순환을 찾는 문제

1. 전수조사를 통해 비용이 가장 작은 순환을 찾는다.
2. 단순 TSP 알고리즘(항상 최적의 해를 가지지 않는다.)
   1. 하나의 정점을 선택하여 출발점으로 한다.
   2. 이 정점에 연결된 연결선의 비용이 가장 작은 정점을 선택한다.
   3. 이 정점에서 아직 선택되지 않은 정점들 중에서 연결선의 비용이 가장 작은 정점을 선택한다.
   4. 모든 정점을 선택할 때까지 2와 3의 절차를 반복한다.
3. 

#### 그래프 채색 문제

- 그래프의 채색
  - 인접하고 있는 정점들은 서로 다른 색을 갖도록 하면서 그래프의 모든정점에 색을 할당
- 색상수
  - 그래프 채색에 필요한 최소한의 색의수
  - x(G) 
- 간단한 방법
  1. 모든 정점들의 순서를 정한다.
  2. 모든 색상들의 순서를 정한다.
  3. 그래프 채색의 조건을 만족하는 색상중에서 가장 낮은 번호의 색상을 선택하여 vi에 배정한다.
- 그리디 알고리즘
  - 결정을 할 때마다 최종 결과에 관계없이 최선의 선택을 한다
  - 그 순간의 선택은 그 순간에서의 최적의 선택이다
  - 최종결과가 최적이라는 보장은 없다.



### 신장 트리

- 모든 정점을 포함하면서 순환이 존재하지 않는 부분 그래프

#### 최소신장트리(MST)

- 가중 그래프에서 가중치의 합을 최소로 하는 신장트리
- 최소 신장 트리 알고리즘 : Prim 알고리즘, Kruskal 알고리즘

#### Prim 알고리즘

- Greedy 알고리즘이지만 모든 그래프에 대해 최적의 해를 구한다.
- 시간복잡도 : O(v2), 구현에 따라 O(v.loge)까지 가능(PriorityQueue)

1. 한 정점을 집합에 넣는다.
2. while(집합으로부터 나가는 선이 없을때 까지)
3. 집합에 포합되지 않는 정점 중에 에지의 가중치가 가장 낮은 정점을 집합에 포함시킨다.

#### Kruskal 알고리즘

1. e의 모든 연결선을 가중치가 적은 순서대로 정렬한다.
2. while(선택한 연결선 수 < 정점의 수 -1)
3. 선택한 연결선이 순환을 만들지 않는 것중 가장 작은 것을 차례대로 선택한다.

- 시간복잡도 : O(E*V)



### 최단 경로 알고리즘

#### Dijkstra 알고리즘

- 방향 그래프, 비방향 그래프 모두 적용
- 에지들은 모두 양의 가중치를 가져야한다.

1. 집합에 시작점을 넣고, 다른 정점들로의 거리 배열에 각 정점으로의 거리를 넣는다.
2. 그 중 가장 작은 정점을 집합에 넣고, 정점을 거쳤을 경우 거리가 더 짧아지는 경우 갱신한다.
   - 이때 갱신되는 점을 저장해 놓는 것이 좋다.
3. 모든 점에 대해서 반복 시행한다.

- 시간복잡도 : 일반적 O(v2), 최적 O(ElogV)



#### Bellman-Ford알고리즘

- 가중치가 음일때도 가능
- 사이클의 가중치의 합은 항상 양수여야 한다.(사이클을 연속으로 돌을 시 무한적으로 가중치가 낮아짐)
- 시간복잡도 : O(VE)

1. 시작점으로부터 각 정점들까지의 거리 배열을 만든다.
2. 시작점은 0 그리고 나머지 정점들은 무한대로 초기화한다.
3. for(각 정점) 시작점으로부터 자신과 연결되어 있는 정점을 거쳐서 오는 거리중 최솟값으로 배열값을 갱신한다. dis[start,j] = min(dis[start,i]+dis[start,j]);
4. 모든 정점에 대해서 값이 갱신되지 않을 때까지 반복한다.
