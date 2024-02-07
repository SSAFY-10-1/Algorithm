# 💠 How-to-solve-week1

## 🐍 1. 백준 3190번 (뱀)

[백준 3190번 infikei 제출 기록 (제출 번호 : 72195318)](https://www.acmicpc.net/status?problem_id=3190&user_id=infikei)

- 우선 보드의 각 칸마다 사과 또는 뱀이 위치하는지를 기록하기 위해 n * n 크기의 2차원 배열 board를 사용했다. 사과가 있는 칸에는 2를 저장하고, 뱀의 몸통이 위치한 칸에는 1을 저장했다.

- 또한 뱀의 머리와 꼬리가 각각 움직이게 되는데, 꼬리는 머리가 지나온 길을 따라 차례대로 움직여야 하기 때문에 큐를 이용하여 지나온 길을 저장했다. 아직 자바의 자료구조에 익숙하지 않기 때문에 우선 Deque 인터페이스와 ArrayDeque 클래스를 큐 대신 활용했다.

- 뱀의 방향 변환 정보는 시간 순서대로 주어지므로 입력을 따로 저장하고 정렬할 필요 없이 그냥 입력 한 줄이 들어올 때마다 이동 및 방향 전환을 처리해주었다. 또한 마지막 입력이 들어온 이후에도 게임이 끝나지 않은 경우, 게임이 끝날 때까지 이동 작업을 추가로 수행했다.

- 뱀의 방향을 바꾸는 작업과 뱀의 머리와 꼬리를 움직이는 작업을 각각 changeDirection() 메서드와 moveSnake() 메서드로 분리하여 중복코드를 제거하고 코드의 가독성을 높였다.

- 자바로 골드 문제를 해결한 적이 많지 않고 최근 백준 폼이 별로이다보니 풀이를 작성하는 데 시간이 다소 소요되었다. 하지만 이번 주에 배운 기본형과 참조형, 인터페이스와 클래스, API 문서를 보는 방법 등등을 알고 나니 자바 언어로 풀이를 작성하는 것에 어느 정도 적응이 된 것 같다. 특히 배열, ArrayList, Deque, ArrayDeque 등을 새롭게 활용할 수 있게 되었다.

## 🍗 2. 백준 15686번 (치킨 배달)

[백준 15686번 infikei 제출 기록 (제출 번호 : 72201313)](https://www.acmicpc.net/status?problem_id=15686&user_id=infikei)

- 처음에 문제를 보고 어떻게 풀어야할지 당황스러웠지만, N과 M의 최댓값이 크지 않아서 완전탐색 풀이로 접근했다.

- dfs() 함수로 재귀를 돌리면서 가능한 모든 경우에 대해 탐색하도록 했다. 특히 각각의 집마다 "치킨 거리"를 구하는 메서드를 calcChickenDistOf() 메서드로 분리하고 하나의 집과 하나의 치킨집 사이의 거리를 구하는 메서드를 calcDistBetween()로 분리하여 코드의 가독성을 높였다.

- 이번 문제를 통해 클래스 내 메서드 분리와 클래스 내 변수 사용에 대해 어느 정도 가이드라인을 잡을 수 있었다.