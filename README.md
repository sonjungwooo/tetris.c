# tetris.c
> 단국대학교부속소프트웨어고등학교 포트폴리오

## 개발동기
성공과 실패를 경험하면서 C언어로 나만의 게임을 꼭 만들고 싶다 마음먹고 테트리스 게임 만들기를 시작하게 되었습니다.
 
## 개발언어 및 개발도구
가장 처음 파이게임으로 슈팅게임을 만들어 본 경험으로 C언어 고급 문법을 사용하여 더욱 완성도 있는 테트리스를 만들고 싶어졌습니다. 평소 가장 많이 사용한 개발 도구 Visual Studio Code로 제작되었습니다.
 
## 개발 진행 과정
가장 먼저, 다른 사람들이 만든 다양한 테트리스 게임들을 해보았습니다. 그리고 개발에 사용된 도형들을 나의 테트리스에 shape라는 구조체 배열 안에 좌표로 적용해 보았습니다. 또한 nFrame이라는 함수를 사용하여 도형이 떨어지는 속도를 조정할 수 있었고 Case문을 이용해 방향키로 도형의 위치를 바꿀 수 있게 했습니다.

## 설명
DrawScreen: 화면 전체를 그리고 게임판과 게임 이름, 벽까지 한꺼번에 그립니다.
DrawBoard: 게임판만 그립니다. 즉 외부벽과 문자열들은 빼고 쌓여 있는 벽 돌만 그립니다.
Processkey: 키 입력을 처리하는데 main 함수의 부담을 덜어주기 위해 별 도의 함수로 분리해 놓았습니다. 이동중인 벽돌이 바닥에 닿으면 TRUE를 리턴합니다.
PrintBrick: 벽돌을 출력하거나 삭제하는데 이동중인 벽돌을 대상으로 하 므로 전역변수 brick, rot, nx, ny값을 참조합니다.
GetAround: 벽돌 주변에 무엇이 있는지 검사하여 벽돌의 이동 및 회전 가능성을 조사합니다. 이동중인 벽돌의 주변을 조사하는 것이 아니므로 인수로 전달된 위치의 벽돌 모양을 참조합니다.
MoveDown: 벽돌을 한칸 아래로 이동시킵니다. 만약 바닥에 닿았다면 TestFull함수를 호출한 후 TRUE를 리턴합니다.
TestFull: 수평으로 다 채워진 줄을 찾아 삭제합니다.
 
## 후기 및 어려운 점 극복하기
 테트리스 게임을 완성하면서 가장 어려웠던 과정은 한 줄이 꽉 채워지면 그 줄이 사라지게 하는 것입니다. 왜냐하면 한 줄이 다 채워졌는지 확인한 후에 그 줄을 삭제하고 위에 있던 줄이 내려오게 해야 하기 때문입니다. 어려움을 극복할 수 있었던 것은 시간이 많이 걸렸지만 최대한 많이 생각하고 여러 가지 방법으로 시도해 보았습니다. 제 목표는 단국대학교부속소프트웨어고등학교를 입학하고 앞으로 게임 엔진을 배우고 사용하는 방법을 익혀 그래픽을 더 멋지게 만들고 많은 사람들이 즐겁게 게임할 수 있도록 발전시키고 싶습니다.
