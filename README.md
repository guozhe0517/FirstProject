# FirstProject
Git은 일정한 작업 흐름의 개념이다. 로컬 저장소와 원격 저장소를 나누어 작업의 효율과 접근성을 높혔고,
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

Working directory -> Stage Area = add
Stage Area -> Local Repository = commit
Local Repository -> Remote Repository = push
Remote repository -> Working directory = pull
Remote Repository -> Local Repository = fetch
Local Repository -> Working Directory = merge
pull = fetch + merge;
Git != Github - github은 remote repository를 지원하는 서비스일 뿐이다.
Github을 깔끔하게 관리해 이력서나 포트폴리오를 대체하도록 할 수 있다.
Git으로 파일들을 관리할 때, 원치 않은 파일들을 제외하고 싶은 경우에는 .Ignore파일을 생성해 활용한다.

협업시 같은 파일의 같은 곳을 임의로 동시에 변경해 충돌이 일어날 수 있다.
항상 pull을 한 후 push하는 것을 원칙으로 하며 충돌이 일어난 경우에는 오류가 난 line을 삭제하거나 정돈해준 후
merge한다.

오류는 HEAD에 저장되어 ==========, ************* 라인 사이에 자리한다.

Branch는 독립적으로 여러 작업을 한 번에 병행할 수 있게 해주는 기능이다.

각각의 이름 default는 원격저장소 - origin 로컬저장소 - master 이다.
클론할 때 받게 될 commit의 위치는 origin / HEAD로 표시된다.

아직 github의 유용성에 대해서 피부로 와닿지 않는다. 어떻게 관리해야 할 지도 감이 안잡힌다.
포괄적인 결론은 내가 작업한 걸 기록으로 남겨 복구하거나 비교할 수 있고,
다른 사람과 나누어 작업하며 서로의 기록을 들여다보고 병합할 수 있는 툴 정도라는 것. 👏👏
01.10 💻

###command line을 활용한 git 관리

source tree -> terminal 버튼을 클릭해 command창을 연다. 🔌

####git 명령어 🔎

 --help == 명령어 보기
 init == .git 폴더를 생성해 관리 시작하기
 status  == 폴더내의 git 상태 확인
 log == 히스토리 확인
 add 파일명 == stage area로 파일 올리기
 commit -m"commit message" = commit하기
 clone 저장주소 == 원격저장소 로컬에 복제하기
 pull == remote 정보를 받아 워킹디렉토리와 병함
 push == remote로 정보 보내기
 ......
 
 pwd  == 현재 경로
 ls == 디렉토리 안의 파일 리스트
 cd == change directory
 cd .. == 상위 폴더로 가기
 cd 디렉토리 주소 == 해당 디렉토리로 이동
 mkdir 디렉토리 명 == 디렉토리 만들기
 via 파일명.확장자 == 파일 생성 및 텍스트 편집기 열기
 (텍스트 편집기 안에서)
 i == 텍스트 삽입 시작
 alt + : q == 종료
 alt + : w == 저장
 alt + : q! == 강제 종료
 .....
 
