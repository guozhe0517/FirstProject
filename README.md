# FirstProject
1.Git 기초
- Git은 일정한 작업 흐름의 개념이다. 로컬 저장소와 원격 저장소를 나누어 작업의 효율과 접근성을 높혔고,
다양한 소프트웨어도구와 결합해 사용되고 있다.
Git에는 3가지 영역이 있다. Working directory, Staging Area, Git directory(Repository).

Working directory는 현재 사용자가 작업하고 있는 공간으로, 대게 사용하고 있는 컴퓨 터의 로컬 folder를 뜻한다.

Staging Area는 준비구역으로 Repository에 최종적으로 commit하기 전에 변경이력을 관리한다.

또한 특정 기준에 따라 선택적인 commit이 가능하다.

한 번 commit을 하면 되돌리기란 매우 까다로워서 이 단계에서 신중히 생각한 후 commit을 누르는 것이 좋다.

commit의 단위는 사용자의 작업 기준에 따라 다르나, 일반적으로 한 기능에 한 번씩 commit하면서 테스트한다.

Repository는 변경이력을 저장해 기록으로 남기는 곳이다. 보통 Local과 Remote 두 곳으로 나뉘어 관리된다.

Local은 작업하고 있는 컴퓨터를 뜻하며 빠른 속도로 요청을 처리한다.
Remote는 원격 서버를 말하며 다중 사용자가 접근해 파일을 관리할 수 있다.
협업의 경우, 각자의 로컬에서 작업하고 Remote에서 병합하게 된다.

각 영역으로의 이동에 따른 용어는 다음과 같다.
