# Github Collaboration

<br><br>

## 목차

1. [소개](#소개)
2. [변수](#변수)
3. [함수](#함수)

<br><br>

## Git Repository 구성 살펴보기

<br>

Repository는 Upstream Remote Repository(이하 Upstream Repository), Origin Remote Repository(이하 Origin Repository), Local Repository 이렇게 3부분으로 구성됩니다. Upstream Repository는 개발자들이 공유하는 저장소로 최신 소스코드가 저장되어 있는 원격 저장소입니다. Origin Repository는 Upstream Repository를 Fork한 원격 개인 저장소입니다. Local Repository는 내 컴퓨터에 저장되어 있는 개인 저장소입니다.

<br>

![image](https://github.com/user-attachments/assets/8a91a764-1af8-433e-95e4-32fcbe9ce21d)

<br>

위 그림은 Git Repository 구성과 워크플로우를 설명하고 있습니다. Local Repository에서 작업을 완료한 한 후 작업 브랜치을 Origin Repository에 push합니다. 그리고 Github에서 Origin Repository에 push한 브랜치를 Upstream Repository로 merge하는 Pull Request를 생성하고 코드리뷰를 거친 후 merge 합니다. 다시 새로운 작업을 할 때 Local Repository에서 Upstream Repository를 pull 합니다.

<br><br>

## Git Branch 전략

<br>

### Git Flow 전략

Git-flow에는 5가지 종류의 브랜치가 존재합니다. 항상 유지되는 메인 브랜치들(master, develop)과 일정 기간 동안만 유지되는 보조 브랜치들(feature, release, hotfix)이 있습니다.

master : 제품으로 출시될 수 있는 브랜치
develop : 다음 출시 버전을 개발하는 브랜치
feature : 기능을 개발하는 브랜치
release : 이번 출시 버전을 준비하는 브랜치
hotfix : 출시 버전에서 발생한 버그를 수정 하는 브랜치

<br>

![image](https://github.com/user-attachments/assets/b9b46826-385f-4aed-abc4-fd3cb2aa32d3)

<br>

처음에는 master와 develop 브랜치가 존재합니다. 물론 develop 브랜치는 master에서부터 시작된 브랜치입니다. develop 브랜치에서는 상시로 버그를 수정한 커밋들이 추가됩니다. 새로운 기능 추가 작업이 있는 경우 develop 브랜치에서 feature 브랜치를 생성합니다. feature 브랜치는 언제나 develop 브랜치에서부터 시작하게 됩니다. 기능 추가 작업이 완료되었다면 feature 브랜치는 develop 브랜치로 merge 됩니다. develop에 이번 버전에 포함되는 모든 기능이 merge 되었다면 QA를 하기 위해 develop 브랜치에서부터 release 브랜치를 생성합니다. QA를 진행하면서 발생한 버그들은 release 브랜치에 수정됩니다. QA를 무사히 통과했다면 release 브랜치를 master와 develop 브랜치로 merge 합니다. 마지막으로 출시된 master 브랜치에서 버전 태그를 추가합니다.

<br><br>

## Github Project

<br>

![image](https://github.com/user-attachments/assets/07dc4f97-5b17-4e08-96ce-72e505809ecd)

<br>

![image](https://github.com/user-attachments/assets/a084a1c8-0af3-4552-a2a4-58e37d251cfd)

<br>

![image](https://github.com/user-attachments/assets/b4124fc5-5eca-446f-a9b9-d5fe0f983ffd)

<br>

![image](https://github.com/user-attachments/assets/16169685-3f7f-401f-bf4f-ee1b4abdc0d6)

<br>

![image](https://github.com/user-attachments/assets/66199853-410d-4cca-b311-dcc2c3055f12)

<br>

1. Assignees (담당자)
설명: 특정 작업이나 이슈를 담당할 팀원 또는 사용자를 지정합니다.
기능: 작업의 책임을 분명히 하여, 누가 해당 작업을 수행해야 하는지를 명확하게 합니다.
2. Status (상태)
설명: 작업이나 이슈의 현재 진행 상태를 나타냅니다.
기능: 일반적으로 "To Do", "In Progress", "Done" 등의 상태로 표시되며, 작업의 진행 상황을 추적하는 데 도움이 됩니다.
3. Priority (우선순위)
설명: 작업이나 이슈의 긴급성과 중요도를 나타냅니다.
기능: P0, P1, P2 등의 등급으로 구분되어, 팀이 어떤 작업을 먼저 처리해야 할지 결정하는 데 도움을 줍니다.
4. Size (크기)
설명: 작업의 크기나 복잡성을 나타내는 메트릭입니다.
기능: 팀이 작업의 양을 가늠하고, 전체 작업 부하를 관리하는 데 사용됩니다. 예를 들어, "Small", "Medium", "Large"와 같은 구분이 있을 수 있습니다.
5. Estimate (추정 시간)
설명: 작업을 완료하는 데 필요한 시간의 추정값입니다.
기능: 작업에 소요될 시간을 예측하고, 프로젝트의 전체 일정을 계획하는 데 유용합니다.
6. Iteration (반복)
설명: 프로젝트의 특정 반복 주기나 스프린트를 나타냅니다.
기능: 애자일 개발 방식에서 스프린트 또는 반복 주기를 정의하여 팀이 특정 기간 동안 어떤 작업을 수행할 것인지 계획하는 데 도움을 줍니다.
7. Start Date (시작일)
설명: 작업이 시작되는 날짜를 나타냅니다.
기능: 작업 일정 관리를 위해 필요한 정보를 제공합니다.
8. End Date (종료일)
설명: 작업이 완료되는 날짜를 나타냅니다.
기능: 프로젝트의 전체 일정과 각 작업의 마감일을 관리하는 데 사용됩니다.

<br>

![image](https://github.com/user-attachments/assets/72c4b6e4-51c6-4e94-bc52-3da476d3cca9)

<br>

![image](https://github.com/user-attachments/assets/c5549905-a04c-4795-960a-2ccebfbf0726)

<br>

![image](https://github.com/user-attachments/assets/9a26b7a1-5272-4859-a3e9-0fc4d59dd3d9)

<br>

![image](https://github.com/user-attachments/assets/21152d87-6ce9-495d-8789-39a458309fa1)

<br>
