# Github Collaboration

<br><br>

## 목차

1. [소개](#소개)
2. [변수](#변수)
3. [함수](#함수)

<br><br>

## Git Repository 구성 살펴보기

Repository는 Upstream Remote Repository(이하 Upstream Repository), Origin Remote Repository(이하 Origin Repository), Local Repository 이렇게 3부분으로 구성됩니다. Upstream Repository는 개발자들이 공유하는 저장소로 최신 소스코드가 저장되어 있는 원격 저장소입니다. Origin Repository는 Upstream Repository를 Fork한 원격 개인 저장소입니다. Local Repository는 내 컴퓨터에 저장되어 있는 개인 저장소입니다.

![image](https://github.com/user-attachments/assets/8a91a764-1af8-433e-95e4-32fcbe9ce21d)

위 그림은 Git Repository 구성과 워크플로우를 설명하고 있습니다. Local Repository에서 작업을 완료한 한 후 작업 브랜치을 Origin Repository에 push합니다. 그리고 Github에서 Origin Repository에 push한 브랜치를 Upstream Repository로 merge하는 Pull Request를 생성하고 코드리뷰를 거친 후 merge 합니다. 다시 새로운 작업을 할 때 Local Repository에서 Upstream Repository를 pull 합니다.

<br>


<br>


<br>

<br><br>

## **기초 개념**

상속, 인터페이스, 오버라이딩
