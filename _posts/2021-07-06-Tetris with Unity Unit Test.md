---
layout: post
title:  "(개인)Tetris with Unity TestFramework"
date:   2021-07-06
excerpt: "유니티 테스트 프레임 워크를 활용한 테트리스"
project: true
tag:
- jekyll 
- moon
- blog
- about
- theme
comments: true
---
<center><b>Tetris</b></center>with Unity TestFramework
     
### 프로젝트 제목
Tetris with Unity TestFramework  

### 프로젝트 기간
2021-07-06

### 프로젝트 목표 및 내용
* 목표
	Unity Test FrameWork를 활용한 테트리스  

* 내용
	Unity Test FrameWork를 이용하여 클라이언트 Unit Test 코드를 작성해보자.  
	Unity 로직과 게임 데이터 로직은 분리하여 게임 코드 테스트를 좀 더 용이하게 하자.  

---

### 팀 규모 및 역할
* 1인 개발


### 나의 역할 및 기술 스택
#### Unity 2020.2.0f1/ C#
* Tetris 로직 개발  
* Tetris UI 개발  
* Unit Test 코드 작성  
* Unity TestFrameWork 연결  


### 이 프로젝트를 통해 배운점
*	Tetris를 만들면서 MVC 패턴을 적용해볼 수 있었다. Unit 테스트를 통해 UI는 테스트하기 어렵다고 느껴 MVC중 Model 부분의 테스트 코드를 작성하였다.  
	이를 위해 Model View 간의 완벽하게 분리하였고, 모든 Model 부분에 대하여 테스트 코드를 작성해볼 수 있었다.  
*	Test 코드를 작성하면서 양 옆으로 넘쳐서 쌓이는 버그를 발견할 수 있었고 버그 수정 후 해당 부분에 대한 테스트 코드를 작성하면서 테스트 코드의 중요성을 깨달았다.  
*	SetBlockStackOnlyDataForTest 과 같이 뒤에 ForTest 가 붙은 테스트를 위한 함수들이 몇개가 만들어졌는데 테스트를 위한 코드를 작성하는것이 과연 옳은 것인가 고민을 했다.   
	이러한 코드를 만드지 않는것이 최선이겠지만  
	어쩔 수 없는 경우에는 partical를 이용하여 class 내 test용 함수 분리하기  
	ForTest가 붙은 코드는 테스트 외 사용금지  
	Attribute를 이용하여 테스트용 함수로만 사용하기  
	등 규칙을 정해서 사용하면 좋을 것 같다라고 생각했다.  
* 	Unity AssemblyDefine을 이용하면 실수로 데이터 코드안에 Unity 함수를 사용하는 실수를 막아준다는 것을 깨달았다.  

---

### 소스 저장소
* [Tetris](https://github.com/Meerkat-GMD/Tetris)

### Preview
*