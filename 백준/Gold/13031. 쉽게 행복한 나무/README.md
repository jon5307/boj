# [Gold III] 쉽게 행복한 나무 - 13031 

[문제 링크](https://www.acmicpc.net/problem/13031) 

### 성능 요약

메모리: 56712 KB, 시간: 260 ms

### 분류

깊이 우선 탐색, 그래프 이론, 그래프 탐색, 그리디 알고리즘, 트리

### 제출 일자

2024년 10월 27일 19:56:54

### 문제 설명

<p>어떤 나무가 있다. 이 나무는 우리가 익히 아는 자료구조인 트리와 같이 생겼는데, 1~N번까지 N개의 정점을 가지고 있다. 1번 정점을 루트로 하는 이 트리에는 각 노드와 간선에는 하나의 숫자가 쓰여져 있다. 민주는 알고리즘 캠프가 끝나고 휴양림을 갔다가 이 나무를 발견했다. 나무를 보던 민주는 문득 나무의 몇몇 정점이 슬퍼보였다. 민주는 알고리즘 캠프가 끝나서 너무 기쁘기 때문에, 몇몇 정점을 잘라 나무를 행복하게 만들어주고 싶다.</p>

<p>어떤 정점 v가 슬프다는 것은 v아래의 부분트리(subtree)들 중 dist(v, u) > au를 만족하는 정점 u가 하나 이상 존재한다는 것이다. 이때 au는 정점 u에 쓰여있는 숫자이며, dist(v, u)는 v에서 u로 가는 경로에 존재하는 간선들에 적힌 숫자들의 합이다.</p>

<p>민주는 키보드보다 무거운 물건은 들 수 없기 때문에, 정점을 자를 때에는 트리의 말단 정점(leaves)만 자를 수 있다. 트리의 말단 정점이란, 해당 정점으로부터 연결된 자식 정점이 존재하지 않는 정점을 말한다. 자세히 설명하자면 말단 정점과 연결된 정점은 해당 정점의 부모 정점밖에 없다. 즉, 연결된 정점이 하나밖에 없는 정점을 말단 노드라고 부를 수 있는데, 그 중 루트 정점은 트리를 구성하는 정점의 개수가 총 1개 -정점 노드밖에 존재하지 않을 때- 에만 말단 정점이라고 할 수 있다.</p>

<p>민주는 이 복잡한 나무가 행복해질 때까지 정점 노드를 자르려고 한다. 이때 민주가 잘라야하는 정점의 최소 개수는 몇 개일까?</p>

<p>아래 그림의 1)과 같은 나무가 있을 때, 이 나무에서 잘려나가는 정점들은 최소는 다음의 2) ~ 6)의 5개가 된다.</p>

<p style="text-align: center;"><img alt="" src="" style="height:425px; width:436px"></p>

### 입력 

 <p>첫 줄에 나무의 노드의 개수 N(1 ≤ N ≤ 100,000)이 주어진다. 두 번째 줄에는 1번 노드부터 N번 노드에 쓰여있는 숫자 a<sub>i</sub>(1 ≤ N ≤ 1,000,000,000)가 N개 주어진다. 다음 N - 1개의 줄에는 각 노드들을 잇는 간선의 정보가 들어온다. i번째 간선 정보는 각각 p<sub>i</sub>(1 ≤ p<sub>i</sub> ≤ N)와 c<sub>i</sub>(0 ≤ c<sub>i</sub> ≤ 1,000,000,000)를 가지는데, 이때 (i + 1)번 노드는 p<sub>i</sub>노드와 연결되어 있고 해당 간선에 쓰인 숫자는 c<sub>i</sub>가 된다.</p>

### 출력 

 <p>한 줄에 나무가 행복해지기 위해 잘라야하는 말단 정점의 최소 개수를 출력하라.</p>

