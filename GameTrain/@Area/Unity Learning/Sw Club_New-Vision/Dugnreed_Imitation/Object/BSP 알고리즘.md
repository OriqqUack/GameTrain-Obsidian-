---
태그: 공부
설명: 던그리드 맵 생성 관련 알고리즘
오늘 날짜: "[[2023-10-09]]"
---

## BSP 알고리즘이란?

- 이진 공간 분할법(BInary Space Partitioning, BSP)은 재귀적으로 유클리드 공간을 초평면 상의 볼록 집합으로 분할하는 기법이다. 분할 과정으로 BSP 트리라 불리는 트리 구조가 만들어진다.

![[Pasted image 20231009151654.png]]

## 알고리즘

- 1. 임의의 방향(수직, 수평)과 임의의 위치를 선택해 공간을 둘로 분할한다.
- 2. 정해진 노드만큼 1번 과정을 반복한다.
- 3. 나누어진 공간에 맞춰 방을 생성한다.
- 4. 트리를 거슬러 올라가 방과 방을 연결한다.


[[알고리즘 스크립트]]

