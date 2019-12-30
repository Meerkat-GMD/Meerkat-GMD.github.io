---
layout: post
title:  "(개인) Unity GameManager"
date:   2019-11-01
excerpt: "UnityEvent 실행관리 툴 및 JSON 스크립트 Editor"
project: true
tag:
- jekyll 
- moon
- blog
- about
- theme
comments: true
---
<center><b>Unity GameManager</b> "UnityEvent 실행관리 툴"</center>
     
### 프로젝트 제목
Unity GameManager

### 프로젝트 기간
2019.11.01 ~ 지속적으로 기능 추가중

### 프로젝트 목표 및 내용
* 목표

	Unity 게임 이벤트를 비슷한것 끼리 묶어 코드의 재사용성을 높이자

* 내용

	GameManager = 각 씬마다 하나씩 존재하며 씬내의 Part의 실행 순서를 조율한다.

	EventManager = 하나의 Part를 맡고 있으며 Part 내부의 이벤트 실행 순서를 조율한다.

	GameEvent = Part 내부에 존재하며 각 Event들을 나열하여 순서대로 진행된다.
	(이벤트 도중에 다음 이벤트 실행이 가능하며 각 이벤트 간의 시작 딜레이, 종료 딜레이 등을 넣을수 있다.) 

	또한 이러한 이벤트들을 손으로 일일히 등록하는 것은 귀찮기 때문에 Custom Editor 기능을 활용하여 자동으로 이벤트 등록하는 기능을 넣음

	JSON Editor를 통해 게임내 들어가는 대사들을 손쉽게 관리함.

---

### 팀 규모 및 역할
* 1인 개발
나재흠 : 툴 시스템 기획 및 필요한 이벤트 기능 개발

### 나의 역할 및 기술 스택
#### Unity 에디터 프로그래밍 / Unity 2019.2.9f1/ C# 
* GameManager 전체적인 설계를 하여 이벤트가 어떻게 실행될것인지 이벤트가 실행되지 않는 동안에는 어떻게 할 것인인지 기획
* GameManager에서 EventMaanger를 List에다가 저장하여 순서대로 실행하게 개발
* EventManager에서 GameEvent를 List에 저장하여 순서대로 실행하게 개발
* GameEvent에서는 Event의 실행단계를 5개로 나누어서 실행함. (모든 게임이벤트는 Game_Event를 상속)
	1. Event_init() = 이벤트 실행하기전 변수 초기화등을 진행함. (각각의 이벤트에서 따로 구현)
	2. Event_Start() = init()이랑 비슷하나 Game_Event에서 구현되어 있으며 모든 이벤트에 적용할 내용이 있을 때 사용
	3. Event_Content() = 이벤트 실행 내용을 적는 곳
	4. Event_Tieup() = 이벤트가 끝나기전 이벤트가 다시 실행될때를 고려하여 변수들을 원래 값으로 돌리거나 메모리 할당 받은것을 해제해주는 곳
	5. Event_Finish() = Tieup()이랑 비슷하나 Game_Event에서 구현되어 있으며 모든 이벤트에 적용할 내용이 있을 때 사용
* Unity Custom Editor 기능을 통해 필요한 변수들만 Inspector 창에 띄우고 이벤트를 자동으로 삽입해주는 기능 개발 
* JSON Editor를 통해 스크립트 수정을 용이하게 함.

### 이 프로젝트를 통해 배운점
* 이전 프로젝트를 진행할 때 비슷한 내용이지만 프로젝트 별로 필요한 코드의 내용이 조금씩 달라 재활용할 수 없는 경우가 있었는데 그러한 점을 해결하여 개발속도가 빨라짐 
이를 통해 재사용 높은 코드를 작성하는게 중요하다는걸 느낌
* 기획의 변경으로 인해 이벤트 실행 순서를 바꾸어야 할 때 코드를 수정하는것이 아닌 오브젝트의 child 순서를 바꾸는 것만으로 실행순서를 바꾸어서 개발속도를 높임
* 대사를 수정할 일이 있을 때 JSON Editor를 통해 안의 내용만 수정함으로써 다시 빌드 할 필요 없이 실행하게 함.

---

### 소스 저장소
* [Unity GameManager](https://github.com/Meerkat-GMD/Unity_GameManager)

### Preview
* 준비중
